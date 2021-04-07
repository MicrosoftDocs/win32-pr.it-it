---
description: La \_ classe CIM bioselement rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per avviare e configurare un sistema di computer.
ms.assetid: c203244a-51e0-4733-a0bc-cf9b7957f364
ms.tgt_platform: multiple
title: Classe CIM_BIOSElement (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Caption
- CIM_BIOSElement.Description
- CIM_BIOSElement.InstallDate
- CIM_BIOSElement.Status
- CIM_BIOSElement.Name
- CIM_BIOSElement.BuildNumber
- CIM_BIOSElement.CodeSet
- CIM_BIOSElement.IdentificationCode
- CIM_BIOSElement.LanguageEdition
- CIM_BIOSElement.OtherTargetOS
- CIM_BIOSElement.SerialNumber
- CIM_BIOSElement.SoftwareElementID
- CIM_BIOSElement.SoftwareElementState
- CIM_BIOSElement.TargetOperatingSystem
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.Version
- CIM_BIOSElement.PrimaryBIOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21cd0d13d62f5cfa70f579110480b4c11c36b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049232"
---
# <a name="cim_bioselement-class-cimwin32-wmi-providers"></a><span data-ttu-id="cbcdf-103">Classe CIM_BIOSElement (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-103">CIM_BIOSElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cbcdf-104">La classe **CIM \_ bioselement** rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per avviare e configurare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-104">The **CIM\_BIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbcdf-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cbcdf-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cbcdf-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cbcdf-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcdf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbcdf-109">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C562-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  string   BuildNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  uint16   TargetOperatingSystem;
  string   Manufacturer;
  string   Version;
  boolean  PrimaryBIOS;
};
```

## <a name="members"></a><span data-ttu-id="cbcdf-110">Members</span><span class="sxs-lookup"><span data-stu-id="cbcdf-110">Members</span></span>

<span data-ttu-id="cbcdf-111">La classe **CIM \_ bioselement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cbcdf-111">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="cbcdf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbcdf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbcdf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cbcdf-113">Properties</span></span>

<span data-ttu-id="cbcdf-114">La classe **CIM \_ bioselement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-114">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbcdf-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-119">Identificatore interno per la compilazione di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="cbcdf-120">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-125">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-125">A short textual description of the object.</span></span>

<span data-ttu-id="cbcdf-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-127">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-131">Set di codici utilizzato dall'elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-131">Code set used by the software element.</span></span>

<span data-ttu-id="cbcdf-132">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-133">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-136">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-137">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-137">A textual description of the object.</span></span>

<span data-ttu-id="cbcdf-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-142">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-143">Identificatore del produttore per l'elemento software, spesso un'unità di supporto (SKU) o un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-143">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="cbcdf-144">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-149">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-149">Indicates when the object was installed.</span></span> <span data-ttu-id="cbcdf-150">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cbcdf-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-155">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-156">Edizione del linguaggio dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-156">Language edition of the software element.</span></span> <span data-ttu-id="cbcdf-157">I codici di lingua definiti in ISO 639 devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="cbcdf-158">Quando l'elemento software rappresenta le versioni multilingue o internazionali di un prodotto, è necessario usare la stringa "Multilingual".</span><span class="sxs-lookup"><span data-stu-id="cbcdf-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="cbcdf-159">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-159">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-160">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-160">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-163">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-164">Produttore del BIOS.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-164">The manufacturer of the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-165">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-165">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-168">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-169">Nome usato per identificare questo elemento software</span><span class="sxs-lookup"><span data-stu-id="cbcdf-169">The name used to identify this software element</span></span>

<span data-ttu-id="cbcdf-170">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-170">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-171">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-171">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-174">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-174">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-175">Produttore e tipo di sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha un valore 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="cbcdf-175">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="cbcdf-176">Se il valore della proprietà **TargetOperatingSystem** è 1, questa proprietà deve avere un valore non null.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-176">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="cbcdf-177">Per tutti gli altri valori **TargetOperatingSystem** , questa proprietà è null.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-177">For all other **TargetOperatingSystem** values, this property is null.</span></span>

<span data-ttu-id="cbcdf-178">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-178">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-179">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-179">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-182">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-183">Se **true**, si tratta del BIOS principale del computer.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-183">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-184">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-184">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-187">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-187">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-188">Numero di serie dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-188">Serial number of the software element.</span></span>

<span data-ttu-id="cbcdf-189">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-189">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-190">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-190">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-193">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-193">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-194">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-194">Identifier for the software element.</span></span> <span data-ttu-id="cbcdf-195">È progettato per essere usato insieme ad altri tasti per creare una rappresentazione univoca di questo [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-195">It is designed to be used in conjunction with other keys to create a unique representation of this [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="cbcdf-196">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-196">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbcdf-197">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-197">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-200">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-200">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-201">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-201">State of a software element.</span></span>

<span data-ttu-id="cbcdf-202">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-202">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="cbcdf-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-203"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-204">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-204">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="cbcdf-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-205"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-206">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-206">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="cbcdf-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-207"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-208">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-208">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="cbcdf-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-209"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-210">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-210">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cbcdf-211">**Status**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-211">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-212">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-214">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-214">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-215">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-215">String that indicates the current status of the object.</span></span> <span data-ttu-id="cbcdf-216">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-216">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cbcdf-217">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="cbcdf-217">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cbcdf-218">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-218">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cbcdf-219">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="cbcdf-219">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cbcdf-220">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-220">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cbcdf-221">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-221">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cbcdf-222">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cbcdf-223">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbcdf-223">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cbcdf-224">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-224">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cbcdf-225">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-225">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cbcdf-226">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="cbcdf-226">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cbcdf-227">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-227">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cbcdf-228">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-228">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cbcdf-229">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-229">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cbcdf-230">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-230">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cbcdf-231">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-231">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cbcdf-232">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-232">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cbcdf-233">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-233">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cbcdf-234">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-234">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cbcdf-235">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-235">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cbcdf-236">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-236">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-239">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| software Component Information \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-239">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-240">Ambiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-240">Operating system environment.</span></span> <span data-ttu-id="cbcdf-241">Il valore di questa proprietà non garantisce l'esecuzione binaria. sono necessarie altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-241">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="cbcdf-242">È necessario specificare la versione del sistema operativo utilizzando il controllo della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-242">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="cbcdf-243">È necessario anche l'architettura in cui viene eseguito il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-243">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="cbcdf-244">La combinazione di questi costrutti consente al provider di identificare chiaramente il livello di sistema operativo necessario per un particolare elemento software.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-244">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="cbcdf-245">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-245">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cbcdf-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cbcdf-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="cbcdf-248"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-248"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-249">Mac OS</span><span class="sxs-lookup"><span data-stu-id="cbcdf-249">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="cbcdf-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-250"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-251">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="cbcdf-251">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="cbcdf-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-252"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="cbcdf-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-253"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="cbcdf-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-254"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="cbcdf-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-255"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-256">Apri VM</span><span class="sxs-lookup"><span data-stu-id="cbcdf-256">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="cbcdf-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-257"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-258">HP-UX</span><span class="sxs-lookup"><span data-stu-id="cbcdf-258">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="cbcdf-259"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-259"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="cbcdf-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-260"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="cbcdf-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-261"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="cbcdf-262"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-262"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="cbcdf-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-263"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-264">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="cbcdf-264">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="cbcdf-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-265"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="cbcdf-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-266"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-267">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="cbcdf-267">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="cbcdf-268"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-268"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-269">Windows 95</span><span class="sxs-lookup"><span data-stu-id="cbcdf-269">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="cbcdf-270"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-270"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-271">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cbcdf-271">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="cbcdf-272"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-272"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-273">Windows NT</span><span class="sxs-lookup"><span data-stu-id="cbcdf-273">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="cbcdf-274"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-274"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-275">Windows CE</span><span class="sxs-lookup"><span data-stu-id="cbcdf-275">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="cbcdf-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-276"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-277">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="cbcdf-277">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="cbcdf-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-278"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="cbcdf-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-279"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="cbcdf-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-280"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="cbcdf-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-281"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="cbcdf-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-282"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="cbcdf-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-283"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="cbcdf-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-284"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="cbcdf-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-285"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="cbcdf-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-286"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="cbcdf-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-287"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="cbcdf-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-288"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="cbcdf-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-289"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-290">Serie A</span><span class="sxs-lookup"><span data-stu-id="cbcdf-290">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="cbcdf-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-291"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-292">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="cbcdf-292">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="cbcdf-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-293"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-294">NT tandem</span><span class="sxs-lookup"><span data-stu-id="cbcdf-294">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="cbcdf-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-295"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-296">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="cbcdf-296">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="cbcdf-297"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-297"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="cbcdf-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-298"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="cbcdf-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-299"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="cbcdf-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-300"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="cbcdf-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-301"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="cbcdf-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-302"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-303">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="cbcdf-303">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="cbcdf-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-304"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="cbcdf-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-305"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="cbcdf-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-306"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="cbcdf-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-307"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-308">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="cbcdf-308">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="cbcdf-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-309"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="cbcdf-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-310"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="cbcdf-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-311"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="cbcdf-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-312"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="cbcdf-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-313"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="cbcdf-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-314"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="cbcdf-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-315"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="cbcdf-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-316"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="cbcdf-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-317"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="cbcdf-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-318"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="cbcdf-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-319"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="cbcdf-320">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="cbcdf-320">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="cbcdf-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-321"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="cbcdf-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-322"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="cbcdf-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-323"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="cbcdf-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-324"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="cbcdf-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="cbcdf-325"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cbcdf-326">**Versione**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-326">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbcdf-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cbcdf-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbcdf-329">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="cbcdf-329">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="cbcdf-330">Versione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-330">The version of the BIOS.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbcdf-331">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbcdf-331">Remarks</span></span>

<span data-ttu-id="cbcdf-332">La classe **CIM \_ bioselement** è derivata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-332">The **CIM\_BIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="cbcdf-333">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-333">WMI does not implement this class.</span></span> <span data-ttu-id="cbcdf-334">Per ulteriori informazioni sulle classi derivate da **CIM \_ bioselement**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cbcdf-334">For more information about classes derived from **CIM\_BIOSElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cbcdf-335">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-335">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cbcdf-336">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cbcdf-336">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbcdf-337">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbcdf-337">Requirements</span></span>



| <span data-ttu-id="cbcdf-338">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbcdf-338">Requirement</span></span> | <span data-ttu-id="cbcdf-339">Valore</span><span class="sxs-lookup"><span data-stu-id="cbcdf-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcdf-340">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbcdf-340">Minimum supported client</span></span><br/> | <span data-ttu-id="cbcdf-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbcdf-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbcdf-342">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbcdf-342">Minimum supported server</span></span><br/> | <span data-ttu-id="cbcdf-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbcdf-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbcdf-344">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cbcdf-344">Namespace</span></span><br/>                | <span data-ttu-id="cbcdf-345">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cbcdf-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbcdf-346">MOF</span><span class="sxs-lookup"><span data-stu-id="cbcdf-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbcdf-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbcdf-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbcdf-348">DLL</span><span class="sxs-lookup"><span data-stu-id="cbcdf-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbcdf-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbcdf-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbcdf-350">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbcdf-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcdf-351">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="cbcdf-351">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

