---
description: La \_ classe CIM VideoBIOSElement rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.
ms.assetid: f23d411f-4781-4727-abd1-61fe1a366bf0
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSElement
- CIM_VideoBIOSElement.BuildNumber
- CIM_VideoBIOSElement.Caption
- CIM_VideoBIOSElement.CodeSet
- CIM_VideoBIOSElement.Description
- CIM_VideoBIOSElement.IdentificationCode
- CIM_VideoBIOSElement.InstallDate
- CIM_VideoBIOSElement.IsShadowed
- CIM_VideoBIOSElement.LanguageEdition
- CIM_VideoBIOSElement.Manufacturer
- CIM_VideoBIOSElement.Name
- CIM_VideoBIOSElement.OtherTargetOS
- CIM_VideoBIOSElement.SerialNumber
- CIM_VideoBIOSElement.SoftwareElementID
- CIM_VideoBIOSElement.SoftwareElementState
- CIM_VideoBIOSElement.Status
- CIM_VideoBIOSElement.TargetOperatingSystem
- CIM_VideoBIOSElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d873b17f0bf0ea123d988d281c0cab728dd50f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966090"
---
# <a name="cim_videobioselement-class"></a><span data-ttu-id="52e49-103">CIM \_ VideoBIOSElement (classe)</span><span class="sxs-lookup"><span data-stu-id="52e49-103">CIM\_VideoBIOSElement class</span></span>

<span data-ttu-id="52e49-104">La classe **CIM \_ VideoBIOSElement** rappresenta il software di basso livello che viene caricato in un archivio non volatile e utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="52e49-104">The **CIM\_VideoBIOSElement** class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="52e49-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="52e49-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="52e49-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="52e49-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="52e49-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="52e49-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="52e49-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="52e49-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e49-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52e49-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{76148BF6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VideoBIOSElement : CIM_SoftwareElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
  boolean  IsShadowed;
  string   LanguageEdition;
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  string   SerialNumber;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="52e49-110">Members</span><span class="sxs-lookup"><span data-stu-id="52e49-110">Members</span></span>

<span data-ttu-id="52e49-111">La classe **CIM \_ VideoBIOSElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="52e49-111">The **CIM\_VideoBIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="52e49-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52e49-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52e49-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52e49-113">Properties</span></span>

<span data-ttu-id="52e49-114">La classe **CIM \_ VideoBIOSElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="52e49-114">The **CIM\_VideoBIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52e49-115">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="52e49-115">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-118">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-119">Identificatore interno per la compilazione di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="52e49-119">Internal identifier for the compilation of this software element.</span></span>

<span data-ttu-id="52e49-120">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-120">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-121">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="52e49-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="52e49-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-125">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="52e49-125">Short textual description of the object.</span></span>

<span data-ttu-id="52e49-126">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-127">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="52e49-127">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="52e49-130">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="52e49-131">Set di codici utilizzato dall'elemento software.</span><span class="sxs-lookup"><span data-stu-id="52e49-131">Code set used by the software element.</span></span>

<span data-ttu-id="52e49-132">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-132">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-133">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="52e49-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-136">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="52e49-136">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-137">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="52e49-137">Textual description of the object.</span></span>

<span data-ttu-id="52e49-138">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-139">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="52e49-139">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-142">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-142">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-143">Identificatore del produttore per l'elemento software, ad esempio uno SKU o un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="52e49-143">Manufacturer's identifier for the software element, such as a stock-keeping unit (SKU) or part number.</span></span>

<span data-ttu-id="52e49-144">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-144">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="52e49-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="52e49-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="52e49-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-149">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="52e49-149">Date and time the object was installed.</span></span> <span data-ttu-id="52e49-150">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="52e49-150">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="52e49-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-152">**Ombreggiatura**</span><span class="sxs-lookup"><span data-stu-id="52e49-152">**IsShadowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-153">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="52e49-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-155">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| video BIOS \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-156">Se **true**, il BIOS del video è nascosto.</span><span class="sxs-lookup"><span data-stu-id="52e49-156">If **TRUE**, the video BIOS is shadowed.</span></span>

</dd> <dt>

<span data-ttu-id="52e49-157">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="52e49-157">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-160">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-160">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-161">Edizione del linguaggio dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="52e49-161">Language edition of the software element.</span></span> <span data-ttu-id="52e49-162">I codici di lingua definiti in ISO 639 devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="52e49-162">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="52e49-163">Quando l'elemento software rappresenta una versione multilingue o internazionale di un prodotto, è necessario usare la stringa "Multilingual".</span><span class="sxs-lookup"><span data-stu-id="52e49-163">When the software element represents a multilingual or international version of a product, the string "Multilingual" should be used.</span></span>

<span data-ttu-id="52e49-164">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-164">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-165">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="52e49-165">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-168">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-168">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-169">Produttore dell'elemento software questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-169">Manufacturer of the software element This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-170">**Nome**</span><span class="sxs-lookup"><span data-stu-id="52e49-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-173">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="52e49-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="52e49-174">Nome usato per identificare l'elemento software questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-174">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-175">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="52e49-175">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-178">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="52e49-178">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-179">Produttore e tipo di sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha un valore 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="52e49-179">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="52e49-180">Se il valore della proprietà **TargetOperatingSystem** è 1, questa proprietà deve avere un valore non null.</span><span class="sxs-lookup"><span data-stu-id="52e49-180">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="52e49-181">Per tutti gli altri valori **TargetOperatingSystem** , questa proprietà è null.</span><span class="sxs-lookup"><span data-stu-id="52e49-181">For all other **TargetOperatingSystem** values, this property is null.</span></span> <span data-ttu-id="52e49-182">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-182">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-183">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="52e49-183">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-186">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-186">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-187">Il numero di serie dell'elemento software è stato assegnato.</span><span class="sxs-lookup"><span data-stu-id="52e49-187">Assigned serial number of the software element.</span></span>

<span data-ttu-id="52e49-188">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-188">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-189">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="52e49-189">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-192">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="52e49-192">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="52e49-193">Identificatore dell'elemento software progettato per essere utilizzato insieme ad altre chiavi per creare una rappresentazione univoca della classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="52e49-193">Identifier for the software element that is designed to be used in conjunction with other keys to create a unique representation of the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

<span data-ttu-id="52e49-194">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-194">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="52e49-195">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="52e49-195">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52e49-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-198">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52e49-198">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52e49-199">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="52e49-199">State of a software element.</span></span>

<span data-ttu-id="52e49-200">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-200">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="52e49-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="52e49-201"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-202">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="52e49-202">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="52e49-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="52e49-203"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-204">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="52e49-204">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="52e49-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="52e49-205"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-206">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="52e49-206">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="52e49-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="52e49-207"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-208">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="52e49-208">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="52e49-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="52e49-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-212">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="52e49-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-213">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="52e49-213">Current status of the object.</span></span> <span data-ttu-id="52e49-214">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="52e49-215">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="52e49-215">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="52e49-216">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="52e49-216">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="52e49-217">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="52e49-217">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="52e49-218">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="52e49-218">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52e49-219">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="52e49-219">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="52e49-220">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="52e49-220">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="52e49-221">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="52e49-221">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="52e49-222">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="52e49-222">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="52e49-223">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="52e49-223">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="52e49-224">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="52e49-224">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="52e49-225">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="52e49-225">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="52e49-226">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="52e49-226">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="52e49-227">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="52e49-227">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52e49-228">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="52e49-228">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-229">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52e49-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-231">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| software Component Information \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="52e49-231">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-232">Ambiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52e49-232">Operating system environment.</span></span> <span data-ttu-id="52e49-233">Il valore di questa proprietà non garantisce l'esecuzione binaria.</span><span class="sxs-lookup"><span data-stu-id="52e49-233">The value of this property does not ensure binary execution.</span></span> <span data-ttu-id="52e49-234">La versione del sistema operativo deve essere specificata utilizzando il controllo della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52e49-234">The version of the operating system must be specified using the operating system version check.</span></span> <span data-ttu-id="52e49-235">È necessario anche l'architettura in cui viene eseguito il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="52e49-235">Also required is the architecture on which the operating system runs.</span></span> <span data-ttu-id="52e49-236">La combinazione di questi costrutti consente al provider di identificare chiaramente il livello di sistema operativo necessario per un particolare elemento software.</span><span class="sxs-lookup"><span data-stu-id="52e49-236">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<span data-ttu-id="52e49-237">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-237">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="52e49-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="52e49-238"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="52e49-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="52e49-239"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="52e49-240"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="52e49-240"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-241">Mac OS</span><span class="sxs-lookup"><span data-stu-id="52e49-241">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="52e49-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="52e49-242"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-243">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="52e49-243">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="52e49-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="52e49-244"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="52e49-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="52e49-245"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="52e49-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="52e49-246"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="52e49-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="52e49-247"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-248">Apri VM</span><span class="sxs-lookup"><span data-stu-id="52e49-248">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="52e49-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="52e49-249"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-250">HP-UX</span><span class="sxs-lookup"><span data-stu-id="52e49-250">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="52e49-251"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="52e49-251"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="52e49-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="52e49-252"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="52e49-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="52e49-253"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="52e49-254"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="52e49-254"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="52e49-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="52e49-255"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-256">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="52e49-256">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="52e49-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="52e49-257"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="52e49-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="52e49-258"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-259">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="52e49-259">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="52e49-260"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="52e49-260"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-261">Windows 95</span><span class="sxs-lookup"><span data-stu-id="52e49-261">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="52e49-262"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="52e49-262"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-263">Windows 98</span><span class="sxs-lookup"><span data-stu-id="52e49-263">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="52e49-264"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="52e49-264"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-265">Windows NT</span><span class="sxs-lookup"><span data-stu-id="52e49-265">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="52e49-266"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="52e49-266"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-267">Windows CE</span><span class="sxs-lookup"><span data-stu-id="52e49-267">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="52e49-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="52e49-268"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-269">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="52e49-269">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="52e49-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="52e49-270"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="52e49-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="52e49-271"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="52e49-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="52e49-272"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="52e49-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="52e49-273"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="52e49-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="52e49-274"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="52e49-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="52e49-275"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="52e49-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="52e49-276"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="52e49-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="52e49-277"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="52e49-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="52e49-278"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="52e49-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="52e49-279"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="52e49-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="52e49-280"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="52e49-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="52e49-281"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-282">Serie A</span><span class="sxs-lookup"><span data-stu-id="52e49-282">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="52e49-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="52e49-283"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-284">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="52e49-284">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="52e49-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="52e49-285"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-286">NT tandem</span><span class="sxs-lookup"><span data-stu-id="52e49-286">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="52e49-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="52e49-287"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-288">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="52e49-288">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="52e49-289"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="52e49-289"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="52e49-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="52e49-290"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="52e49-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="52e49-291"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="52e49-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="52e49-292"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="52e49-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="52e49-293"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="52e49-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="52e49-294"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-295">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="52e49-295">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="52e49-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="52e49-296"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="52e49-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="52e49-297"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="52e49-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="52e49-298"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="52e49-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="52e49-299"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-300">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="52e49-300">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="52e49-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="52e49-301"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="52e49-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="52e49-302"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="52e49-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="52e49-303"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="52e49-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="52e49-304"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="52e49-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="52e49-305"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="52e49-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="52e49-306"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="52e49-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="52e49-307"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="52e49-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="52e49-308"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="52e49-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="52e49-309"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="52e49-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="52e49-310"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="52e49-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="52e49-311"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="52e49-312">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="52e49-312">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="52e49-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="52e49-313"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="52e49-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="52e49-314"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="52e49-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="52e49-315"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="52e49-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="52e49-316"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="52e49-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="52e49-317"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="52e49-318">**Versione**</span><span class="sxs-lookup"><span data-stu-id="52e49-318">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52e49-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52e49-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52e49-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52e49-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52e49-321">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="52e49-321">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="52e49-322">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="52e49-322">Version of the operation.</span></span>

<span data-ttu-id="52e49-323">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="52e49-323">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="52e49-324"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="52e49-324"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="52e49-325"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="52e49-325"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="52e49-326">Questa proprietà viene ereditata dalla classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="52e49-326">This property is inherited from the [**CIM\_SoftwareElement**](cim-softwareelement.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52e49-327">Commenti</span><span class="sxs-lookup"><span data-stu-id="52e49-327">Remarks</span></span>

<span data-ttu-id="52e49-328">La classe **CIM \_ VideoBIOSElement** è derivata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="52e49-328">The **CIM\_VideoBIOSElement** class is derived from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="52e49-329">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="52e49-329">WMI does not implement this class.</span></span>

<span data-ttu-id="52e49-330">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="52e49-330">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="52e49-331">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="52e49-331">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e49-332">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52e49-332">Requirements</span></span>



| <span data-ttu-id="52e49-333">Requisito</span><span class="sxs-lookup"><span data-stu-id="52e49-333">Requirement</span></span> | <span data-ttu-id="52e49-334">Valore</span><span class="sxs-lookup"><span data-stu-id="52e49-334">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52e49-335">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52e49-335">Minimum supported client</span></span><br/> | <span data-ttu-id="52e49-336">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52e49-336">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52e49-337">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52e49-337">Minimum supported server</span></span><br/> | <span data-ttu-id="52e49-338">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52e49-338">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52e49-339">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52e49-339">Namespace</span></span><br/>                | <span data-ttu-id="52e49-340">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="52e49-340">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52e49-341">MOF</span><span class="sxs-lookup"><span data-stu-id="52e49-341">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52e49-342"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52e49-342"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52e49-343">DLL</span><span class="sxs-lookup"><span data-stu-id="52e49-343">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52e49-344"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52e49-344"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e49-345">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52e49-345">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e49-346">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="52e49-346">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

