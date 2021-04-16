---
description: Rappresenta gli attributi del BIOS (Basic Input/output Services) del computer installati in un computer.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Classe Win32_BIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524113"
---
# <a name="win32_bios-class"></a><span data-ttu-id="26899-103">\_Classe BIOS Win32</span><span class="sxs-lookup"><span data-stu-id="26899-103">Win32\_BIOS class</span></span>

<span data-ttu-id="26899-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BIOS Win32** rappresenta gli attributi del BIOS (Basic Input/output Services) del computer installato in un computer.</span><span class="sxs-lookup"><span data-stu-id="26899-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="26899-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="26899-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="26899-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="26899-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26899-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26899-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="26899-108">Members</span><span class="sxs-lookup"><span data-stu-id="26899-108">Members</span></span>

<span data-ttu-id="26899-109">La **classe \_ BIOS Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26899-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="26899-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26899-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26899-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26899-111">Properties</span></span>

<span data-ttu-id="26899-112">La **classe \_ BIOS Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26899-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26899-113">**BiosCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="26899-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-114">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="26899-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-116">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 0 \| BIOS caratteristiche")</span><span class="sxs-lookup"><span data-stu-id="26899-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="26899-117">Matrice di caratteristiche BIOS supportate dal sistema come definito dalla specifica di riferimento del BIOS di System Management.</span><span class="sxs-lookup"><span data-stu-id="26899-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="26899-118">Questo valore deriva dal membro **caratteristiche BIOS** della struttura di **informazioni del BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-119">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="26899-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="26899-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="26899-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="26899-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (1)</span><span class="sxs-lookup"><span data-stu-id="26899-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26899-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="26899-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="26899-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Caratteristiche BIOS non supportate** (3)</span><span class="sxs-lookup"><span data-stu-id="26899-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="26899-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA è supportato** (4)</span><span class="sxs-lookup"><span data-stu-id="26899-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="26899-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA è supportato** (5)</span><span class="sxs-lookup"><span data-stu-id="26899-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="26899-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA è supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="26899-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="26899-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI è supportato** (7)</span><span class="sxs-lookup"><span data-stu-id="26899-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="26899-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Scheda PC (PCMCIA) supportata** (8)</span><span class="sxs-lookup"><span data-stu-id="26899-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="26899-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play è supportato** (9)</span><span class="sxs-lookup"><span data-stu-id="26899-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="26899-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM è supportato** (10)</span><span class="sxs-lookup"><span data-stu-id="26899-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="26899-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>Il **BIOS è aggiornabile (Flash)** (11)</span><span class="sxs-lookup"><span data-stu-id="26899-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="26899-132">Il BIOS è aggiornabile (Flash)</span><span class="sxs-lookup"><span data-stu-id="26899-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="26899-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>Lo **shadowing del BIOS è consentito** (12)</span><span class="sxs-lookup"><span data-stu-id="26899-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="26899-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA è supportato** (13)</span><span class="sxs-lookup"><span data-stu-id="26899-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="26899-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>Il **supporto per ESCD è disponibile** (14)</span><span class="sxs-lookup"><span data-stu-id="26899-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="26899-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>L' **avvio da CD è supportato** (15)</span><span class="sxs-lookup"><span data-stu-id="26899-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="26899-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>L' **avvio selezionabile è supportato** (16)</span><span class="sxs-lookup"><span data-stu-id="26899-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="26899-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**ROM BIOS è socketed** (17)</span><span class="sxs-lookup"><span data-stu-id="26899-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="26899-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>L' **avvio dalla scheda PC (PCMCIA) è supportato** (18)</span><span class="sxs-lookup"><span data-stu-id="26899-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="26899-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**La specifica EDD (Enhanced Disk Drive) è supportata** (19)</span><span class="sxs-lookup"><span data-stu-id="26899-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="26899-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h-floppy giapponese per NEC 9800 1.2 MB (3,5 \\ ", 1K byte/settore, 360 rpm) è supportato** (20)</span><span class="sxs-lookup"><span data-stu-id="26899-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="26899-142">Int 13h-floppy giapponese per NEC 9800 1.2 MB (3,5, 1K byte/settore, 360 RPM) è supportato</span><span class="sxs-lookup"><span data-stu-id="26899-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="26899-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h-floppy giapponese per Toshiba 1.2 MB (3,5 \\ ", 360 rpm) è supportato** (21)</span><span class="sxs-lookup"><span data-stu-id="26899-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="26899-144">Int 13h-floppy giapponese per Toshiba 1.2 MB (3,5, 360 RPM) è supportato</span><span class="sxs-lookup"><span data-stu-id="26899-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**I servizi floppy Int 13h-5,25 \\ "/360 KB sono supportati** (22)</span><span class="sxs-lookup"><span data-stu-id="26899-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="26899-146">I servizi floppy Int 13h-5,25/360 KB sono supportati</span><span class="sxs-lookup"><span data-stu-id="26899-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/1.2MB i servizi floppy sono supportati** (23)</span><span class="sxs-lookup"><span data-stu-id="26899-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="26899-148">Sono supportati i servizi floppy Int 13h-5,25/1.2MB</span><span class="sxs-lookup"><span data-stu-id="26899-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="26899-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**I servizi floppy Int 13h-3,5 \\ "/720 KB sono supportati** (24)</span><span class="sxs-lookup"><span data-stu-id="26899-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="26899-150">I servizi floppy Int 13h-3,5/720 KB sono supportati</span><span class="sxs-lookup"><span data-stu-id="26899-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**\\ Sono supportati i servizi floppy Int 13h-3,5 "/2,88 MB** (25)</span><span class="sxs-lookup"><span data-stu-id="26899-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="26899-152">Sono supportati i servizi floppy Int 13h-3,5/2,88 MB</span><span class="sxs-lookup"><span data-stu-id="26899-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="26899-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, il servizio Print Screen è supportato** (26)</span><span class="sxs-lookup"><span data-stu-id="26899-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 i servizi di tastiera sono supportati** (27)</span><span class="sxs-lookup"><span data-stu-id="26899-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, i servizi seriali sono supportati** (28)</span><span class="sxs-lookup"><span data-stu-id="26899-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, i servizi stampanti sono supportati** (29)</span><span class="sxs-lookup"><span data-stu-id="26899-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="26899-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Sono supportati i servizi video int 10h, CGA/mono** (30)</span><span class="sxs-lookup"><span data-stu-id="26899-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="26899-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span><span class="sxs-lookup"><span data-stu-id="26899-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="26899-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**Supportato da ACPI** (32)</span><span class="sxs-lookup"><span data-stu-id="26899-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="26899-160">ACPI è supportato</span><span class="sxs-lookup"><span data-stu-id="26899-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="26899-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**Legacy USB supportata** (33)</span><span class="sxs-lookup"><span data-stu-id="26899-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="26899-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP è supportato** (34)</span><span class="sxs-lookup"><span data-stu-id="26899-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="26899-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>L' **avvio di I2O è supportato** (35)</span><span class="sxs-lookup"><span data-stu-id="26899-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="26899-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**È supportato l'avvio LS-120** (36)</span><span class="sxs-lookup"><span data-stu-id="26899-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="26899-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>L' **avvio dell'unità ZIP ATAPI è supportato** (37)</span><span class="sxs-lookup"><span data-stu-id="26899-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="26899-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 avvio supportato** (38)</span><span class="sxs-lookup"><span data-stu-id="26899-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="26899-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Batteria intelligente supportata** (39)</span><span class="sxs-lookup"><span data-stu-id="26899-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="26899-168">La batteria intelligente è supportata</span><span class="sxs-lookup"><span data-stu-id="26899-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="26899-169">40 47</span><span class="sxs-lookup"><span data-stu-id="26899-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="26899-170">Riservato per Fornitore BIOS</span><span class="sxs-lookup"><span data-stu-id="26899-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="26899-171">48 63</span><span class="sxs-lookup"><span data-stu-id="26899-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="26899-172">Riservato per il fornitore del sistema</span><span class="sxs-lookup"><span data-stu-id="26899-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26899-173">**BIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-174">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="26899-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26899-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26899-176">Matrice delle informazioni complete sul BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="26899-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="26899-177">In molti computer possono essere presenti diverse stringhe di versione archiviate nel registro di sistema e rappresentano le informazioni del BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="26899-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="26899-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="26899-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-181">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="26899-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="26899-182">Identificatore interno per questa compilazione di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="26899-183">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-184">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="26899-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-187">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="26899-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="26899-188">Breve descrizione dell'oggetto stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="26899-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="26899-189">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-190">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="26899-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-193">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="26899-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="26899-194">Set di codici utilizzato da questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-194">Code set used by this software element.</span></span>

<span data-ttu-id="26899-195">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-196">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="26899-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-199">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 13 \| Current Language")</span><span class="sxs-lookup"><span data-stu-id="26899-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="26899-200">Nome della lingua del BIOS corrente.</span><span class="sxs-lookup"><span data-stu-id="26899-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="26899-201">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="26899-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-204">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="26899-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="26899-205">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26899-205">Description of the object.</span></span>

<span data-ttu-id="26899-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-207">**EmbeddedControllerMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-208">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="26899-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26899-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-210">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| embedded controller firmware major release")</span><span class="sxs-lookup"><span data-stu-id="26899-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="26899-211">Versione principale del firmware del controller incorporato.</span><span class="sxs-lookup"><span data-stu-id="26899-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="26899-212">Questo valore deriva dal membro della **versione principale del firmware del controller incorporato** della struttura di **informazioni del BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-213">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="26899-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="26899-214">**EmbeddedControllerMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-215">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="26899-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26899-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-217">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| embedded controller firmware minor release")</span><span class="sxs-lookup"><span data-stu-id="26899-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="26899-218">Versione secondaria del firmware del controller incorporato.</span><span class="sxs-lookup"><span data-stu-id="26899-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="26899-219">Questo valore deriva dal membro della **versione secondaria del firmware del controller incorporato** della struttura di **informazioni del BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-220">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="26899-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="26899-221">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="26899-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-224">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="26899-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="26899-225">Identificatore del produttore di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="26899-226">Spesso si tratta di una SKU (Stock Keeping Unit) o di un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="26899-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="26899-227">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-228">**InstallableLanguages**</span><span class="sxs-lookup"><span data-stu-id="26899-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-229">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26899-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-231">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| Installable languages")</span><span class="sxs-lookup"><span data-stu-id="26899-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="26899-232">Numero di lingue disponibili per l'installazione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="26899-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="26899-233">Il linguaggio può determinare proprietà quali la necessità di testo in formato Unicode e bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="26899-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="26899-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="26899-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-235">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26899-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26899-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-237">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="26899-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="26899-238">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26899-238">Date and time the object was installed.</span></span> <span data-ttu-id="26899-239">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="26899-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="26899-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-241">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="26899-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-244">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="26899-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="26899-245">Edizione della lingua di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-245">Language edition of this software element.</span></span> <span data-ttu-id="26899-246">I codici di lingua definiti in ISO 639 devono essere usati.</span><span class="sxs-lookup"><span data-stu-id="26899-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="26899-247">Quando l'elemento software rappresenta una versione multilingue o internazionale di un prodotto, è necessario usare la stringa "Multilingual".</span><span class="sxs-lookup"><span data-stu-id="26899-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="26899-248">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-249">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="26899-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-250">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="26899-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="26899-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-252">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 13 \| language strings")</span><span class="sxs-lookup"><span data-stu-id="26899-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="26899-253">Matrice di nomi di lingue disponibili che è possibile installare nel BIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="26899-254">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="26899-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-255">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-257">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="26899-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="26899-258">Produttore di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="26899-259">Questo valore deriva dal membro del **Fornitore** della struttura di **informazioni del BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-260">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-261">**Nome**</span><span class="sxs-lookup"><span data-stu-id="26899-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-264">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="26899-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="26899-265">Nome utilizzato per identificare questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-265">Name used to identify this software element.</span></span>

<span data-ttu-id="26899-266">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-267">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="26899-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-270">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="26899-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="26899-271">Registra il produttore e il tipo di sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha un valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="26899-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="26899-272">Se il valore di **TargetOperatingSystem** è 1, **OtherTargetOS** deve avere un valore non null.</span><span class="sxs-lookup"><span data-stu-id="26899-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="26899-273">Per tutti gli altri valori di **TargetOperatingSystem**, **OtherTargetOS** è **null**.</span><span class="sxs-lookup"><span data-stu-id="26899-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="26899-274">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-275">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="26899-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-276">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26899-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26899-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-278">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| BIOS di sistema \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="26899-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="26899-279">Se **true**, si tratta del BIOS principale del computer.</span><span class="sxs-lookup"><span data-stu-id="26899-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="26899-280">Questa proprietà viene ereditata da [**CIM \_ bioselement**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-281">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="26899-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-282">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26899-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26899-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26899-284">Data di rilascio del BIOS di Windows nel formato UTC (Coordinated Universal Time) di ad aaaammgghhmmss. MMMMMM (+-) OOO.</span><span class="sxs-lookup"><span data-stu-id="26899-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="26899-285">Questo valore deriva dal membro della **Data di rilascio del BIOS** della struttura di informazioni del **BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="26899-286">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="26899-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-289">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="26899-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="26899-290">Il numero di serie dell'elemento software è stato assegnato.</span><span class="sxs-lookup"><span data-stu-id="26899-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="26899-291">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-292">**SMBIOSBIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-295">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 0 \| BIOS Version")</span><span class="sxs-lookup"><span data-stu-id="26899-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="26899-296">Versione BIOS indicata da SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="26899-297">Questo valore deriva dal membro della **versione BIOS** della struttura di **informazioni del BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="26899-298">**SMBIOSMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-299">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26899-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-301">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="26899-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="26899-302">Numero di versione principale di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-302">Major SMBIOS version number.</span></span> <span data-ttu-id="26899-303">Questa proprietà è **null** se SMBIOS non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="26899-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="26899-304">**SMBIOSMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-305">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26899-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-307">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="26899-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="26899-308">Numero di versione secondario di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="26899-309">Questa proprietà è **null** se SMBIOS non viene trovato.</span><span class="sxs-lookup"><span data-stu-id="26899-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="26899-310">**SMBIOSPresent**</span><span class="sxs-lookup"><span data-stu-id="26899-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-311">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26899-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26899-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-313">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| init")</span><span class="sxs-lookup"><span data-stu-id="26899-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="26899-314">Se **true**, il SMBIOS è disponibile in questo computer.</span><span class="sxs-lookup"><span data-stu-id="26899-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="26899-315">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="26899-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-318">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="26899-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="26899-319">Identificatore per questo elemento software; progettato per essere utilizzato insieme ad altri tasti per creare una rappresentazione univoca di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="26899-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="26899-320">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26899-321">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="26899-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-322">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26899-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-324">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26899-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26899-325">Stato di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="26899-325">State of a software element.</span></span>

<span data-ttu-id="26899-326">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="26899-327">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="26899-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="26899-328">**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="26899-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="26899-329">**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="26899-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="26899-330">**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="26899-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="26899-331">**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="26899-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26899-332">**Status**</span><span class="sxs-lookup"><span data-stu-id="26899-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-335">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="26899-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="26899-336">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="26899-336">Current status of the object.</span></span> <span data-ttu-id="26899-337">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="26899-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="26899-338">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="26899-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="26899-339">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="26899-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="26899-340">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="26899-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="26899-341">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="26899-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="26899-342">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="26899-343">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="26899-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="26899-344">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="26899-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="26899-345">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="26899-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26899-346">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="26899-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26899-347">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="26899-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="26899-348">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="26899-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="26899-349">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="26899-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="26899-350">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="26899-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="26899-351">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="26899-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="26899-352">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="26899-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="26899-353">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="26899-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="26899-354">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="26899-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="26899-355">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="26899-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26899-356">**SystemBiosMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-357">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="26899-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26899-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-359">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 0 \| System BIOS principale Release")</span><span class="sxs-lookup"><span data-stu-id="26899-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="26899-360">Il rilascio principale del BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="26899-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="26899-361">Questo valore deriva dal membro della **versione principale del BIOS di sistema** della struttura di informazioni del **BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-362">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="26899-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="26899-363">**SystemBiosMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="26899-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-364">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="26899-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="26899-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-366">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| System BIOS minor release")</span><span class="sxs-lookup"><span data-stu-id="26899-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="26899-367">Versione secondaria del BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="26899-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="26899-368">Questo valore deriva dal membro della **versione secondaria del BIOS di sistema** della struttura di informazioni del **BIOS** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="26899-369">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="26899-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="26899-370">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="26899-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-371">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26899-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26899-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-373">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| software Component Information \| 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="26899-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="26899-374">Sistema operativo di destinazione dell'elemento software proprietario.</span><span class="sxs-lookup"><span data-stu-id="26899-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="26899-375">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="26899-376">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="26899-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26899-377">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="26899-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26899-378">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="26899-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="26899-379">**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="26899-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="26899-380">**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="26899-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="26899-381">**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="26899-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="26899-382">**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="26899-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="26899-383">**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="26899-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="26899-384">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="26899-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="26899-385">**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="26899-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="26899-386">**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="26899-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="26899-387">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="26899-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="26899-388">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="26899-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="26899-389">**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="26899-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="26899-390">**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="26899-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="26899-391">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="26899-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="26899-392">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="26899-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="26899-393">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="26899-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="26899-394">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="26899-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="26899-395">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="26899-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="26899-396">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="26899-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="26899-397">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="26899-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="26899-398">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="26899-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="26899-399">**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="26899-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="26899-400">**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="26899-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="26899-401">**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="26899-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="26899-402">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="26899-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="26899-403">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="26899-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="26899-404">**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="26899-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="26899-405">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="26899-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="26899-406">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="26899-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="26899-407">**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="26899-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="26899-408">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="26899-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="26899-409">**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="26899-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="26899-410">**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="26899-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="26899-411">**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="26899-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="26899-412">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="26899-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="26899-413">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="26899-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="26899-414">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="26899-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="26899-415">**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="26899-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="26899-416">**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="26899-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="26899-417">**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="26899-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="26899-418">**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="26899-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="26899-419">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="26899-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="26899-420">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="26899-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="26899-421">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="26899-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="26899-422">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="26899-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="26899-423">**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="26899-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="26899-424">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="26899-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="26899-425">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="26899-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="26899-426">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="26899-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="26899-427">**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="26899-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="26899-428">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="26899-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="26899-429">**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="26899-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="26899-430">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="26899-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="26899-431">**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="26899-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="26899-432">**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="26899-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="26899-433">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="26899-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="26899-434">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="26899-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="26899-435">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="26899-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="26899-436">**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="26899-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="26899-437">**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="26899-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="26899-438">**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="26899-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26899-439">**Versione**</span><span class="sxs-lookup"><span data-stu-id="26899-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26899-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26899-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26899-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26899-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26899-442">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \| SystemBIOSVersion")</span><span class="sxs-lookup"><span data-stu-id="26899-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="26899-443">Versione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-443">Version of the BIOS.</span></span> <span data-ttu-id="26899-444">Questa stringa viene creata dal produttore del BIOS.</span><span class="sxs-lookup"><span data-stu-id="26899-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="26899-445">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26899-446">Commenti</span><span class="sxs-lookup"><span data-stu-id="26899-446">Remarks</span></span>

<span data-ttu-id="26899-447">La **classe \_ BIOS Win32** è derivata da [**CIM \_ bioselement**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="26899-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="26899-448">Le proprietà nella classe **\_ BIOS Win32** possono cambiare per un computer specifico con lo stesso BIOS, ad esempio l'avvio tramite una modalità BIOS legacy e l'avvio tramite la modalità BIOS UEFI.</span><span class="sxs-lookup"><span data-stu-id="26899-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="26899-449">Tuttavia, le proprietà recuperate dalle strutture SMBIOS devono rimanere invariate.</span><span class="sxs-lookup"><span data-stu-id="26899-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="26899-450">Esempio</span><span class="sxs-lookup"><span data-stu-id="26899-450">Examples</span></span>

<span data-ttu-id="26899-451">L'esempio relativo a [Get-ComputerInfo-query computer da computer locale/remoto-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell nella raccolta TechNet usa una serie di chiamate a hardware e software, incluso il **\_ BIOS Win32**, per visualizzare informazioni su un sistema locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="26899-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="26899-452">L'esempio di [generazione delle informazioni di sistema come VBScript della gerarchia XML](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) nella raccolta TechNet utilizza una serie di chiamate a hardware e software, incluso il **\_ BIOS Win32**, per generare una rappresentazione XML di un sistema utilizzando un output XML manuale.</span><span class="sxs-lookup"><span data-stu-id="26899-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="26899-453">L'esempio di codice PowerShell seguente usa il **\_ BIOS Win32** per restituire le caratteristiche del BIOS</span><span class="sxs-lookup"><span data-stu-id="26899-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="26899-454">Nell'esempio di codice precedente vengono restituite le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="26899-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="26899-455">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26899-455">Requirements</span></span>



| <span data-ttu-id="26899-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="26899-456">Requirement</span></span> | <span data-ttu-id="26899-457">Valore</span><span class="sxs-lookup"><span data-stu-id="26899-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26899-458">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26899-458">Minimum supported client</span></span><br/> | <span data-ttu-id="26899-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26899-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26899-460">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26899-460">Minimum supported server</span></span><br/> | <span data-ttu-id="26899-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26899-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26899-462">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26899-462">Namespace</span></span><br/>                | <span data-ttu-id="26899-463">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="26899-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26899-464">MOF</span><span class="sxs-lookup"><span data-stu-id="26899-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26899-465"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26899-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26899-466">DLL</span><span class="sxs-lookup"><span data-stu-id="26899-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26899-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26899-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26899-468">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26899-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26899-469">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="26899-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="26899-470">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="26899-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

