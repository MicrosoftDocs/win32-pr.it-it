---
description: Rappresenta il software di basso livello caricato nell'archiviazione non volatile e utilizzato per avviare e configurare un sistema di computer (CIM \_ ComputerSystem).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f97cbb495fb8105be012c44942aeedb39377e3d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319527"
---
# <a name="cim_bioselement-class-hyper-v-management"></a><span data-ttu-id="4b0d4-103">Classe CIM_BIOSElement (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4b0d4-103">CIM_BIOSElement class (Hyper-V management)</span></span>

<span data-ttu-id="4b0d4-104">Rappresenta il software di basso livello caricato nell'archiviazione non volatile e utilizzato per avviare e configurare un sistema di computer ([**CIM \_ ComputerSystem**](cim-computersystem.md)).</span><span class="sxs-lookup"><span data-stu-id="4b0d4-104">Represents the low-level software that is loaded into non-volatile storage and used to start up and configure a computer system ([**CIM\_ComputerSystem**](cim-computersystem.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b0d4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b0d4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a><span data-ttu-id="4b0d4-106">Members</span><span class="sxs-lookup"><span data-stu-id="4b0d4-106">Members</span></span>

<span data-ttu-id="4b0d4-107">La classe **CIM \_ bioselement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b0d4-107">The **CIM\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="4b0d4-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b0d4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b0d4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b0d4-109">Properties</span></span>

<span data-ttu-id="4b0d4-110">La classe **CIM \_ bioselement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-110">The **CIM\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b0d4-111">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-111">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ bioselement**.**ListOfLanguages**")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSElement**.**ListOfLanguages**")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-115">Lingua attualmente selezionata per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-115">The currently selected language for the BIOS.</span></span> <span data-ttu-id="4b0d4-116">Queste informazioni possono essere ottenute da System Management BIOS (SMBIOS) utilizzando l'attributo della lingua corrente della struttura di tipo 13 da indicizzare nell'elenco di stringhe che segue la struttura.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-116">This information can be obtained from the System Management BIOS (SMBIOS) using the Current Language attribute of the Type 13 structure to index into the string list that follows the structure.</span></span> <span data-ttu-id="4b0d4-117">Questa proprietà viene formattata con il nome della lingua ISO 639 e può essere seguita dal nome del territorio ISO 3166 e dal metodo di codifica.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-117">This property is formatted using the ISO 639 Language Name, and may be followed by the ISO 3166 Territory Name and the encoding method.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-118">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-118">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-119">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-121">Elenco di lingue installabili per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-121">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="4b0d4-122">Queste informazioni possono essere ottenute da SMBIOS, dall'elenco di stringhe che segue la struttura di tipo 13.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-122">This information can be obtained from SMBIOS, from the string list that follows the Type 13 structure.</span></span> <span data-ttu-id="4b0d4-123">Per specificare le lingue installabili del BIOS, è necessario usare un nome di lingua ISO 639.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-123">An ISO 639 Language Name should be used to specify the BIOS' installable languages.</span></span> <span data-ttu-id="4b0d4-124">È possibile specificare anche il nome del territorio ISO 3166 e il metodo di codifica, dopo il nome della lingua.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-124">The ISO 3166 Territory Name and the encoding method may also be specified, following the Language Name.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-125">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-125">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-129">Indirizzo finale della memoria occupata dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-129">The ending address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-130">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-130">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-131">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-133">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-134">Indirizzo iniziale della memoria occupata dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-134">The starting address of the memory that is occupied by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-135">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-135">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-138">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-139">Stringa in formato libero che descrive l'utilità Flash/Load BIOS necessaria per aggiornare l'oggetto **CIM \_ bioselement** .</span><span class="sxs-lookup"><span data-stu-id="4b0d4-139">A free form string that describes the BIOS flash/load utility that is required to update the **CIM\_BIOSElement** object.</span></span> <span data-ttu-id="4b0d4-140">La versione e altre informazioni possono essere indicate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-140">Version and other information may be indicated in this property.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-141">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-141">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-144">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-145">Produttore dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-145">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-146">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-146">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-149">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-150">True se si tratta del BIOS principale del computer. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-150">True if this is the primary BIOS of the computer system; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-151">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-151">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-152">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-154">Il percorso di pubblicazione dei registri degli attributi BIOS a cui è conforme l'implementazione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-154">The publication location of the BIOS attribute registries to which the BIOS implementation complies.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-155">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-155">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-156">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-158">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-159">Data in cui è stato rilasciato il BIOS.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-159">The Date on which this BIOS was released.</span></span>

</dd> <dt>

<span data-ttu-id="4b0d4-160">**Versione**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-160">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b0d4-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b0d4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b0d4-163">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="4b0d4-163">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="4b0d4-164">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4b0d4-164">The version of the operation.</span></span> <span data-ttu-id="4b0d4-165">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="4b0d4-165">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="4b0d4-166">*<major>*.*<minor>*.*<revision>*</span><span class="sxs-lookup"><span data-stu-id="4b0d4-166">*<major>*.*<minor>*.*<revision>*</span></span>
-   <span data-ttu-id="4b0d4-167">*<major>*.*<minor><letter><revision>*</span><span class="sxs-lookup"><span data-stu-id="4b0d4-167">*<major>*.*<minor><letter><revision>*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b0d4-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b0d4-168">Requirements</span></span>



| <span data-ttu-id="4b0d4-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b0d4-169">Requirement</span></span> | <span data-ttu-id="4b0d4-170">Valore</span><span class="sxs-lookup"><span data-stu-id="4b0d4-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0d4-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b0d4-171">Minimum supported client</span></span><br/> | <span data-ttu-id="4b0d4-172">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4b0d4-172">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4b0d4-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b0d4-173">Minimum supported server</span></span><br/> | <span data-ttu-id="4b0d4-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b0d4-174">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4b0d4-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b0d4-175">Namespace</span></span><br/>                | <span data-ttu-id="4b0d4-176">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b0d4-176">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b0d4-177">MOF</span><span class="sxs-lookup"><span data-stu-id="4b0d4-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b0d4-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b0d4-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b0d4-179">DLL</span><span class="sxs-lookup"><span data-stu-id="4b0d4-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b0d4-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b0d4-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b0d4-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b0d4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b0d4-182">**\_Software CIM**</span><span class="sxs-lookup"><span data-stu-id="4b0d4-182">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> </dl>

 

