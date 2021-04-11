---
description: La \_ classe CIM SoftwareElement scompone un \_ oggetto SoftwareFeature CIM in un set di parti gestibili o distribuibile singolarmente per una determinata piattaforma.
ms.assetid: b2418735-b738-411a-a620-acc31662f824
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElement (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.Caption
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.Description
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.InstallDate
- CIM_SoftwareElement.LanguageEdition
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.Status
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fbe64ddfcf81a7410f5654db89c2924a8eabacc3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126931"
---
# <a name="cim_softwareelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="ec41f-103">Classe CIM_SoftwareElement (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ec41f-103">CIM_SoftwareElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ec41f-104">La classe **CIM \_ SoftwareElement** scompone un oggetto [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) in un set di parti gestibili o distribuibile singolarmente per una determinata piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ec41f-104">The **CIM\_SoftwareElement** class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="ec41f-105">La piattaforma di un elemento software viene identificata in modo univoco dall'architettura hardware e dal sistema operativo sottostanti.</span><span class="sxs-lookup"><span data-stu-id="ec41f-105">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

<span data-ttu-id="ec41f-106">Per comprendere i dettagli del modo in cui viene fornita la funzionalità di una particolare funzionalità software in una determinata piattaforma, gli oggetti **CIM \_ SoftwareElement** a cui fanno riferimento le associazioni [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) sono organizzati in set non contigui basati sulla proprietà **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="ec41f-106">As such, to understand the details of how the functionality of a particular software feature is provided on a particular platform, the **CIM\_SoftwareElement** objects referenced by [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) associations are organized in disjoint sets based on the **TargetOperatingSystem** property.</span></span> <span data-ttu-id="ec41f-107">Un oggetto **CIM \_ SoftwareElement** acquisisce i dettagli di gestione di una parte o di un componente in uno dei quattro stati caratterizzati dalla proprietà **SoftwareElementState** .</span><span class="sxs-lookup"><span data-stu-id="ec41f-107">A **CIM\_SoftwareElement** object captures the management details of a part or component in one of four states characterized by the **SoftwareElementState** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec41f-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ec41f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ec41f-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ec41f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ec41f-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ec41f-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ec41f-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ec41f-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec41f-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec41f-112">Syntax</span></span>

``` syntax
[abstract, UUID("{8502C561-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   Description;
  string   IdentificationCode;
  datetime InstallDate;
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

## <a name="members"></a><span data-ttu-id="ec41f-113">Members</span><span class="sxs-lookup"><span data-stu-id="ec41f-113">Members</span></span>

<span data-ttu-id="ec41f-114">La classe **CIM \_ SoftwareElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ec41f-114">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ec41f-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec41f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec41f-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec41f-116">Properties</span></span>

<span data-ttu-id="ec41f-117">La classe **CIM \_ SoftwareElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ec41f-117">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec41f-118">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="ec41f-118">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-121">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-122">Identificatore interno per la compilazione di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-122">Internal identifier for the compilation of this software element.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ec41f-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-126">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ec41f-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-127">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec41f-127">Short textual description of the object.</span></span>

<span data-ttu-id="ec41f-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-129">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="ec41f-129">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-132">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ec41f-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-133">Set di codici utilizzato dall'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-133">Code set used by the software element.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-134">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ec41f-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-137">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ec41f-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-138">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec41f-138">Textual description of the object.</span></span>

<span data-ttu-id="ec41f-139">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-140">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="ec41f-140">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-143">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-143">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-144">Identificatore del produttore per l'elemento software, spesso un'unità di supporto (SKU) o un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="ec41f-144">Manufacturer's identifier for the software element, often a stock-keeping unit (SKU) or part number.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ec41f-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-146">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ec41f-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-148">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-149">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec41f-149">Date and time the object was installed.</span></span> <span data-ttu-id="ec41f-150">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="ec41f-150">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ec41f-151">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-152">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="ec41f-152">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-155">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-155">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-156">Edizione del linguaggio dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-156">Language edition of the software element.</span></span> <span data-ttu-id="ec41f-157">I codici di lingua definiti in ISO 639 devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="ec41f-157">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="ec41f-158">Quando l'elemento software rappresenta le versioni multilingue o internazionali di un prodotto, è necessario usare la stringa "Multilingual".</span><span class="sxs-lookup"><span data-stu-id="ec41f-158">Where the software element represents multilingual or international versions of a product, the string "multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-159">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="ec41f-159">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-162">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-162">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-163">Produttore dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-163">Manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-164">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ec41f-164">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-167">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ec41f-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-168">Nome usato per identificare l'elemento software questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-168">Name used to identify the software element This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-169">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="ec41f-169">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="ec41f-172">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-173">Produttore e tipo di sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha un valore 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="ec41f-173">Manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 ("Other").</span></span> <span data-ttu-id="ec41f-174">Se il valore della proprietà **TargetOperatingSystem** è 1, questa proprietà deve avere un valore non null.</span><span class="sxs-lookup"><span data-stu-id="ec41f-174">When the **TargetOperatingSystem** property has a value of 1, this property must have a non-null value.</span></span> <span data-ttu-id="ec41f-175">Per tutti gli altri valori **TargetOperatingSystem** , questa proprietà è null.</span><span class="sxs-lookup"><span data-stu-id="ec41f-175">For all other **TargetOperatingSystem** values, this property is null.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-176">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="ec41f-176">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-179">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-179">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-180">Numero di serie dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-180">Serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-181">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="ec41f-181">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-184">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ec41f-184">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-185">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-185">Identifier for the software element.</span></span> <span data-ttu-id="ec41f-186">È progettato per essere usato insieme ad altri tasti per creare una rappresentazione univoca di questo **CIM \_ SoftwareElement**.</span><span class="sxs-lookup"><span data-stu-id="ec41f-186">It is designed to be used in conjunction with other keys to create a unique representation of this **CIM\_SoftwareElement**.</span></span>

</dd> <dt>

<span data-ttu-id="ec41f-187">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="ec41f-187">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-188">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec41f-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-190">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec41f-190">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-191">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-191">State of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="ec41f-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="ec41f-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-193">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="ec41f-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="ec41f-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-195">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="ec41f-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="ec41f-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-197">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="ec41f-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="ec41f-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-199">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="ec41f-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec41f-200">**Status**</span><span class="sxs-lookup"><span data-stu-id="ec41f-200">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-203">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ec41f-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-204">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec41f-204">Current status of the object.</span></span>

<span data-ttu-id="ec41f-205">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ec41f-206">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ec41f-206">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ec41f-207">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ec41f-207">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ec41f-208">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="ec41f-208">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ec41f-209">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="ec41f-209">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec41f-210">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ec41f-210">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ec41f-211">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="ec41f-211">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ec41f-212">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="ec41f-212">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ec41f-213">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="ec41f-213">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ec41f-214">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="ec41f-214">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ec41f-215">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="ec41f-215">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ec41f-216">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="ec41f-216">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ec41f-217">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="ec41f-217">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ec41f-218">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="ec41f-218">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec41f-219">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="ec41f-219">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-220">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec41f-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-222">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| software Component Information \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="ec41f-222">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-223">Ambiente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-223">Operating system environment.</span></span> <span data-ttu-id="ec41f-224">Il valore di questa proprietà non garantisce l'esecuzione binaria. sono necessarie altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ec41f-224">The value of this property does not ensure binary executability, more information is needed.</span></span> <span data-ttu-id="ec41f-225">È necessario specificare la versione del sistema operativo utilizzando il controllo della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-225">The operating system version must be specified using the operating system version check.</span></span> <span data-ttu-id="ec41f-226">È necessario anche l'architettura in cui viene eseguito il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec41f-226">Also needed, is the architecture on which the operating system runs.</span></span> <span data-ttu-id="ec41f-227">La combinazione di questi costrutti consente al provider di identificare chiaramente il livello di sistema operativo necessario per un particolare elemento software.</span><span class="sxs-lookup"><span data-stu-id="ec41f-227">The combination of these constructs allows the provider to clearly identify the level of operating system required for a particular software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec41f-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ec41f-228"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec41f-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ec41f-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="ec41f-230"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="ec41f-230"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-231">Mac OS</span><span class="sxs-lookup"><span data-stu-id="ec41f-231">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="ec41f-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="ec41f-232"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-233">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="ec41f-233">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="ec41f-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="ec41f-234"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="ec41f-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="ec41f-235"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="ec41f-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="ec41f-236"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="ec41f-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="ec41f-237"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-238">Apri VM</span><span class="sxs-lookup"><span data-stu-id="ec41f-238">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="ec41f-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="ec41f-239"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-240">HP-UX</span><span class="sxs-lookup"><span data-stu-id="ec41f-240">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="ec41f-241"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="ec41f-241"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="ec41f-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="ec41f-242"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="ec41f-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="ec41f-243"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="ec41f-244"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="ec41f-244"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="ec41f-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="ec41f-245"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-246">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="ec41f-246">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="ec41f-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="ec41f-247"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="ec41f-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="ec41f-248"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-249">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="ec41f-249">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="ec41f-250"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="ec41f-250"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-251">Windows 95</span><span class="sxs-lookup"><span data-stu-id="ec41f-251">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="ec41f-252"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="ec41f-252"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-253">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ec41f-253">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="ec41f-254"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="ec41f-254"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-255">Windows NT</span><span class="sxs-lookup"><span data-stu-id="ec41f-255">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="ec41f-256"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="ec41f-256"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-257">Windows CE</span><span class="sxs-lookup"><span data-stu-id="ec41f-257">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="ec41f-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="ec41f-258"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-259">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="ec41f-259">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="ec41f-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="ec41f-260"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="ec41f-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="ec41f-261"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="ec41f-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="ec41f-262"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="ec41f-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="ec41f-263"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="ec41f-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="ec41f-264"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="ec41f-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="ec41f-265"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="ec41f-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="ec41f-266"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="ec41f-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="ec41f-267"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="ec41f-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="ec41f-268"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="ec41f-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="ec41f-269"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="ec41f-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="ec41f-270"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="ec41f-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="ec41f-271"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-272">Serie A</span><span class="sxs-lookup"><span data-stu-id="ec41f-272">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="ec41f-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="ec41f-273"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-274">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="ec41f-274">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="ec41f-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="ec41f-275"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-276">NT tandem</span><span class="sxs-lookup"><span data-stu-id="ec41f-276">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="ec41f-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="ec41f-277"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-278">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="ec41f-278">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="ec41f-279"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="ec41f-279"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="ec41f-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="ec41f-280"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="ec41f-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="ec41f-281"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="ec41f-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="ec41f-282"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="ec41f-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="ec41f-283"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="ec41f-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="ec41f-284"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-285">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="ec41f-285">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="ec41f-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="ec41f-286"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="ec41f-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="ec41f-287"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="ec41f-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="ec41f-288"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="ec41f-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="ec41f-289"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-290">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="ec41f-290">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="ec41f-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="ec41f-291"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="ec41f-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="ec41f-292"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="ec41f-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="ec41f-293"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="ec41f-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="ec41f-294"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="ec41f-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="ec41f-295"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="ec41f-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="ec41f-296"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="ec41f-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="ec41f-297"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="ec41f-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="ec41f-298"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="ec41f-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="ec41f-299"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="ec41f-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="ec41f-300"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="ec41f-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="ec41f-301"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ec41f-302">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="ec41f-302">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="ec41f-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="ec41f-303"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="ec41f-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="ec41f-304"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="ec41f-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="ec41f-305"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="ec41f-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="ec41f-306"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="ec41f-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="ec41f-307"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec41f-308">**Versione**</span><span class="sxs-lookup"><span data-stu-id="ec41f-308">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec41f-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec41f-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec41f-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec41f-311">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="ec41f-311">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="ec41f-312">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ec41f-312">Version of the operation.</span></span>

<span data-ttu-id="ec41f-313">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="ec41f-313">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="ec41f-314"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="ec41f-314"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="ec41f-315"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="ec41f-315"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec41f-316">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec41f-316">Remarks</span></span>

<span data-ttu-id="ec41f-317">La classe **CIM \_ SoftwareElement** deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-317">The **CIM\_SoftwareElement** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="ec41f-318">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ec41f-318">WMI does not implement this class.</span></span> <span data-ttu-id="ec41f-319">Per le classi WMI derivate da **CIM \_ SoftwareElement**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ec41f-319">For WMI classes derived from **CIM\_SoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ec41f-320">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ec41f-320">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ec41f-321">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ec41f-321">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec41f-322">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec41f-322">Requirements</span></span>



| <span data-ttu-id="ec41f-323">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec41f-323">Requirement</span></span> | <span data-ttu-id="ec41f-324">Valore</span><span class="sxs-lookup"><span data-stu-id="ec41f-324">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec41f-325">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec41f-325">Minimum supported client</span></span><br/> | <span data-ttu-id="ec41f-326">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec41f-326">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec41f-327">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec41f-327">Minimum supported server</span></span><br/> | <span data-ttu-id="ec41f-328">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec41f-328">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec41f-329">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec41f-329">Namespace</span></span><br/>                | <span data-ttu-id="ec41f-330">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ec41f-330">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec41f-331">MOF</span><span class="sxs-lookup"><span data-stu-id="ec41f-331">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec41f-332"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec41f-332"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec41f-333">DLL</span><span class="sxs-lookup"><span data-stu-id="ec41f-333">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec41f-334"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec41f-334"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec41f-335">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec41f-335">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec41f-336">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="ec41f-336">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

