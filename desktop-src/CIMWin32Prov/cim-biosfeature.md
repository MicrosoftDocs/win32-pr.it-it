---
description: Rappresenta le funzionalità del software di basso livello utilizzato per avviare e configurare un sistema di computer.
ms.assetid: 54d03539-d908-4571-b8fd-934b972e8d84
ms.tgt_platform: multiple
title: Classe CIM_BIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeature
- CIM_BIOSFeature.Caption
- CIM_BIOSFeature.Description
- CIM_BIOSFeature.InstallDate
- CIM_BIOSFeature.Status
- CIM_BIOSFeature.IdentifyingNumber
- CIM_BIOSFeature.ProductName
- CIM_BIOSFeature.Vendor
- CIM_BIOSFeature.Version
- CIM_BIOSFeature.Name
- CIM_BIOSFeature.CharacteristicDescriptions
- CIM_BIOSFeature.Characteristics
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 538dc9e4c18d976901519ae0e2d6f5249fd25c35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878061"
---
# <a name="cim_biosfeature-class"></a><span data-ttu-id="a7503-103">CIM \_ BIOSFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="a7503-103">CIM\_BIOSFeature class</span></span>

<span data-ttu-id="a7503-104">La classe **CIM \_ BIOSFeature** rappresenta le funzionalità del software di basso livello utilizzato per avviare e configurare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="a7503-104">The **CIM\_BIOSFeature** class represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7503-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a7503-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7503-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7503-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7503-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a7503-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a7503-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a7503-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7503-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7503-109">Syntax</span></span>

``` syntax
[UUID("{7D33100E-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   IdentifyingNumber;
  string   ProductName;
  string   Vendor;
  string   Version;
  string   Name;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="a7503-110">Members</span><span class="sxs-lookup"><span data-stu-id="a7503-110">Members</span></span>

<span data-ttu-id="a7503-111">La classe **CIM \_ BIOSFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a7503-111">The **CIM\_BIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="a7503-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7503-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a7503-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a7503-113">Properties</span></span>

<span data-ttu-id="a7503-114">La classe **CIM \_ BIOSFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a7503-114">The **CIM\_BIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a7503-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a7503-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a7503-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7503-119">A short textual description of the object.</span></span>

<span data-ttu-id="a7503-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a7503-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-122">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a7503-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a7503-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-124">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS caratteristica \| 003,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**Caratteristiche**")</span><span class="sxs-lookup"><span data-stu-id="a7503-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-125">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate delle funzionalità BIOS indicate nella matrice di **caratteristiche** .</span><span class="sxs-lookup"><span data-stu-id="a7503-125">Array of free-form strings that provides detailed explanations of the BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="a7503-126">Ogni voce in questa matrice è correlata alla voce nella matrice di **caratteristiche** , che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="a7503-126">Each entry in this array is related to the entry in the **Characteristics** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="a7503-127">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="a7503-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-128">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a7503-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a7503-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-130">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS caratteristica \| 003,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="a7503-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|BIOS Characteristic\|003.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-131">Matrice di Integer che specifica le funzionalità supportate dal BIOS.</span><span class="sxs-lookup"><span data-stu-id="a7503-131">Array of integers that specifies the features supported by the BIOS.</span></span> <span data-ttu-id="a7503-132">Il valore 3 non è valido nello schema CIM perché rappresenta che non sono supportate funzionalità BIOS in DMI.</span><span class="sxs-lookup"><span data-stu-id="a7503-132">The value 3 is not valid in the CIM schema because it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="a7503-133">In tal caso, non è necessario creare un'istanza di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7503-133">In which case, this object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a7503-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a7503-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-135">Altro.</span><span class="sxs-lookup"><span data-stu-id="a7503-135">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7503-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="a7503-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-137">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a7503-137">Unknown.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="a7503-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Non **definito** (3)</span><span class="sxs-lookup"><span data-stu-id="a7503-138"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-139">Non definito.</span><span class="sxs-lookup"><span data-stu-id="a7503-139">Undefined.</span></span>

</dd> <dt>

<span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>

<span data-ttu-id="a7503-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**Supporto ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="a7503-140"><span id="ISA_Support"></span><span id="isa_support"></span><span id="ISA_SUPPORT"></span>**ISA Support** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-141">Supporto ISA.</span><span class="sxs-lookup"><span data-stu-id="a7503-141">ISA support.</span></span>

</dd> <dt>

<span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>

<span data-ttu-id="a7503-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**Supporto per MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="a7503-142"><span id="MCA_Support"></span><span id="mca_support"></span><span id="MCA_SUPPORT"></span>**MCA Support** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-143">Supporto per MCA.</span><span class="sxs-lookup"><span data-stu-id="a7503-143">MCA support.</span></span>

</dd> <dt>

<span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>

<span data-ttu-id="a7503-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**Supporto EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="a7503-144"><span id="EISA_Support"></span><span id="eisa_support"></span><span id="EISA_SUPPORT"></span>**EISA Support** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-145">Supporto EISA.</span><span class="sxs-lookup"><span data-stu-id="a7503-145">EISA support.</span></span>

</dd> <dt>

<span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>

<span data-ttu-id="a7503-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**Supporto PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="a7503-146"><span id="PCI_Support"></span><span id="pci_support"></span><span id="PCI_SUPPORT"></span>**PCI Support** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-147">Supporto PCI.</span><span class="sxs-lookup"><span data-stu-id="a7503-147">PCI support.</span></span>

</dd> <dt>

<span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>

<span data-ttu-id="a7503-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**Supporto PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="a7503-148"><span id="PCMCIA_Support"></span><span id="pcmcia_support"></span><span id="PCMCIA_SUPPORT"></span>**PCMCIA Support** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-149">Supporto PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="a7503-149">PCMCIA support.</span></span>

</dd> <dt>

<span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>

<span data-ttu-id="a7503-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**Supporto PNP** (9)</span><span class="sxs-lookup"><span data-stu-id="a7503-150"><span id="PnP_Support"></span><span id="pnp_support"></span><span id="PNP_SUPPORT"></span>**PnP Support** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-151">Supporto PnP.</span><span class="sxs-lookup"><span data-stu-id="a7503-151">PnP support.</span></span>

</dd> <dt>

<span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>

<span data-ttu-id="a7503-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**Supporto APM** (10)</span><span class="sxs-lookup"><span data-stu-id="a7503-152"><span id="APM_Support"></span><span id="apm_support"></span><span id="APM_SUPPORT"></span>**APM Support** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-153">Supporto APM.</span><span class="sxs-lookup"><span data-stu-id="a7503-153">APM support.</span></span>

</dd> <dt>

<span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>

<span data-ttu-id="a7503-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**BIOS aggiornabile** (11)</span><span class="sxs-lookup"><span data-stu-id="a7503-154"><span id="Upgradeable_BIOS"></span><span id="upgradeable_bios"></span><span id="UPGRADEABLE_BIOS"></span>**Upgradeable BIOS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-155">BIOS aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="a7503-155">Upgradeable BIOS.</span></span>

</dd> <dt>

<span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="a7503-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**Shadowing del BIOS consentito** (12)</span><span class="sxs-lookup"><span data-stu-id="a7503-156"><span id="BIOS_Shadowing_Allowed"></span><span id="bios_shadowing_allowed"></span><span id="BIOS_SHADOWING_ALLOWED"></span>**BIOS Shadowing Allowed** (12)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-157">Shadowing del BIOS consentito.</span><span class="sxs-lookup"><span data-stu-id="a7503-157">BIOS shadowing allowed.</span></span>

</dd> <dt>

<span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>

<span data-ttu-id="a7503-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**Supporto di VL VESA** (13)</span><span class="sxs-lookup"><span data-stu-id="a7503-158"><span id="VL_VESA_Support"></span><span id="vl_vesa_support"></span><span id="VL_VESA_SUPPORT"></span>**VL VESA Support** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-159">Supporto di VL VESA.</span><span class="sxs-lookup"><span data-stu-id="a7503-159">VL VESA support.</span></span>

</dd> <dt>

<span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>

<span data-ttu-id="a7503-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**Supporto di ESCD** (14)</span><span class="sxs-lookup"><span data-stu-id="a7503-160"><span id="ESCD_Support"></span><span id="escd_support"></span><span id="ESCD_SUPPORT"></span>**ESCD Support** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-161">Supporto di ESCD.</span><span class="sxs-lookup"><span data-stu-id="a7503-161">ESCD support.</span></span>

</dd> <dt>

<span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>

<span data-ttu-id="a7503-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**Supporto per LS-120** (15)</span><span class="sxs-lookup"><span data-stu-id="a7503-162"><span id="LS-120_Support"></span><span id="ls-120_support"></span><span id="LS-120_SUPPORT"></span>**LS-120 Support** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-163">Supporto per LS-120.</span><span class="sxs-lookup"><span data-stu-id="a7503-163">LS-120 support.</span></span>

</dd> <dt>

<span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>

<span data-ttu-id="a7503-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**Supporto ACPI** (16)</span><span class="sxs-lookup"><span data-stu-id="a7503-164"><span id="ACPI_Support"></span><span id="acpi_support"></span><span id="ACPI_SUPPORT"></span>**ACPI Support** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-165">Supporto ACPI.</span><span class="sxs-lookup"><span data-stu-id="a7503-165">ACPI support.</span></span>

</dd> <dt>

<span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>

<span data-ttu-id="a7503-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**Supporto** per l'avvio di I2O (17)</span><span class="sxs-lookup"><span data-stu-id="a7503-166"><span id="I2O_Boot_Support"></span><span id="i2o_boot_support"></span><span id="I2O_BOOT_SUPPORT"></span>**I2O Boot Support** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-167">Supporto per l'avvio di I2O.</span><span class="sxs-lookup"><span data-stu-id="a7503-167">I2O boot support.</span></span>

</dd> <dt>

<span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>

<span data-ttu-id="a7503-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**Supporto USB Legacy** (18)</span><span class="sxs-lookup"><span data-stu-id="a7503-168"><span id="USB_Legacy_Support"></span><span id="usb_legacy_support"></span><span id="USB_LEGACY_SUPPORT"></span>**USB Legacy Support** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-169">Supporto USB legacy.</span><span class="sxs-lookup"><span data-stu-id="a7503-169">USB legacy support.</span></span>

</dd> <dt>

<span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>

<span data-ttu-id="a7503-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**Supporto per AGP** (19)</span><span class="sxs-lookup"><span data-stu-id="a7503-170"><span id="AGP_Support"></span><span id="agp_support"></span><span id="AGP_SUPPORT"></span>**AGP Support** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-171">Supporto per AGP.</span><span class="sxs-lookup"><span data-stu-id="a7503-171">AGP support.</span></span>

</dd> <dt>

<span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>

<span data-ttu-id="a7503-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**Scheda PC** (20)</span><span class="sxs-lookup"><span data-stu-id="a7503-172"><span id="PC_Card"></span><span id="pc_card"></span><span id="PC_CARD"></span>**PC Card** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-173">Scheda PC.</span><span class="sxs-lookup"><span data-stu-id="a7503-173">PC card.</span></span>

</dd> <dt>

<span id="IR"></span><span id="ir"></span>

<span data-ttu-id="a7503-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span><span class="sxs-lookup"><span data-stu-id="a7503-174"><span id="IR"></span><span id="ir"></span>**IR** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-175">Integrazione.</span><span class="sxs-lookup"><span data-stu-id="a7503-175">IR.</span></span>

</dd> <dt>

<span id="1394"></span>

<span data-ttu-id="a7503-176"><span id="1394"></span>**1394** (22)</span><span class="sxs-lookup"><span data-stu-id="a7503-176"><span id="1394"></span>**1394** (22)</span></span>


</dt> <dd>

1394.

</dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="a7503-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span><span class="sxs-lookup"><span data-stu-id="a7503-177"><span id="I2C"></span><span id="i2c"></span>**I2C** (23)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-178">I2C.</span><span class="sxs-lookup"><span data-stu-id="a7503-178">I2C.</span></span>

</dd> <dt>

<span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>

<span data-ttu-id="a7503-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span><span class="sxs-lookup"><span data-stu-id="a7503-179"><span id="Smart_Battery"></span><span id="smart_battery"></span><span id="SMART_BATTERY"></span>**Smart Battery** (24)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-180">Batteria intelligente.</span><span class="sxs-lookup"><span data-stu-id="a7503-180">Smart battery.</span></span>

</dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="a7503-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="a7503-181"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)</span></span>


</dt> <dd>

<span data-ttu-id="a7503-182">PC-98.</span><span class="sxs-lookup"><span data-stu-id="a7503-182">PC-98.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a7503-183">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a7503-183">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-186">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a7503-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-187">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7503-187">A textual description of the object.</span></span>

<span data-ttu-id="a7503-188">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-189">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="a7503-189">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-192">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="a7503-192">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-193">Identificazione del prodotto, ad esempio un numero di serie del software o un numero di dado su un chip hardware.</span><span class="sxs-lookup"><span data-stu-id="a7503-193">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

<span data-ttu-id="a7503-194">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-194">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a7503-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-196">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a7503-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-198">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a7503-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-199">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a7503-199">Indicates when the object was installed.</span></span> <span data-ttu-id="a7503-200">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a7503-200">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a7503-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a7503-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-205">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a7503-205">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a7503-206">La proprietà Name definisce l'etichetta in base alla quale l'oggetto è noto al mondo all'esterno del sistema di elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a7503-206">The Name property defines the label by which the object is known to the world outside the data processing system.</span></span> <span data-ttu-id="a7503-207">Questa etichetta è un nome leggibile che identifica in modo univoco l'elemento nel contesto dello spazio dei nomi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a7503-207">This label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="a7503-208">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-208">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-209">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a7503-209">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-212">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a7503-212">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-213">Nome del prodotto comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="a7503-213">Commonly used product name.</span></span>

<span data-ttu-id="a7503-214">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-214">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-215">**Status**</span><span class="sxs-lookup"><span data-stu-id="a7503-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-218">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a7503-218">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-219">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a7503-219">String that indicates the current status of the object.</span></span> <span data-ttu-id="a7503-220">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a7503-220">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a7503-221">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a7503-221">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a7503-222">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a7503-222">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a7503-223">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a7503-223">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a7503-224">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a7503-224">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a7503-225">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a7503-225">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a7503-226">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-226">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a7503-227">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7503-227">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a7503-228">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a7503-228">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a7503-229">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a7503-229">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a7503-230">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a7503-230">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a7503-231">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a7503-231">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a7503-232">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a7503-232">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a7503-233">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a7503-233">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a7503-234">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a7503-234">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a7503-235">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a7503-235">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a7503-236">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a7503-236">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a7503-237">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a7503-237">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a7503-238">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a7503-238">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a7503-239">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a7503-239">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a7503-240">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="a7503-240">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-243">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Vendor**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a7503-243">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-244">Nome del fornitore del prodotto, che corrisponde alla proprietà del **Fornitore** nell'oggetto prodotto dello standard di scambio della soluzione DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7503-244">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="a7503-245">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-245">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7503-246">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a7503-246">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a7503-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a7503-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a7503-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a7503-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a7503-249">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a7503-249">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a7503-250">Informazioni sulla versione del prodotto, che corrisponde alla proprietà **Version** nell'oggetto Product dello standard di scambio della soluzione DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7503-250">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

<span data-ttu-id="a7503-251">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-251">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7503-252">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7503-252">Remarks</span></span>

<span data-ttu-id="a7503-253">La classe **CIM \_ BIOSFeature** è derivata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="a7503-253">The **CIM\_BIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="a7503-254">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a7503-254">WMI does not implement this class.</span></span>

<span data-ttu-id="a7503-255">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7503-255">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7503-256">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a7503-256">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7503-257">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7503-257">Requirements</span></span>



| <span data-ttu-id="a7503-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7503-258">Requirement</span></span> | <span data-ttu-id="a7503-259">Valore</span><span class="sxs-lookup"><span data-stu-id="a7503-259">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7503-260">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7503-260">Minimum supported client</span></span><br/> | <span data-ttu-id="a7503-261">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7503-261">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7503-262">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7503-262">Minimum supported server</span></span><br/> | <span data-ttu-id="a7503-263">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7503-263">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7503-264">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7503-264">Namespace</span></span><br/>                | <span data-ttu-id="a7503-265">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a7503-265">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7503-266">MOF</span><span class="sxs-lookup"><span data-stu-id="a7503-266">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7503-267"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7503-267"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7503-268">DLL</span><span class="sxs-lookup"><span data-stu-id="a7503-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7503-269"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7503-269"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7503-270">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7503-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7503-271">**\_SoftwareFeature CIM**</span><span class="sxs-lookup"><span data-stu-id="a7503-271">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

