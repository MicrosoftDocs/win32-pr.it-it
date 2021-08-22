---
description: Rappresenta gli attributi dei servizi di input/output (BIOS) di base del computer installati in un computer.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Win32_BIOS classe
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
ms.openlocfilehash: bda0a1a07de4411b9a8c683fb2c7e84156b658361df4f2eaf3aa5709c6d11a95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504291"
---
# <a name="win32_bios-class"></a>Classe BIOS Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DEL BIOS Win32** rappresenta gli attributi dei servizi di input/output (BIOS) di base del computer installati in un computer.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

La **classe \_ BIOS Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BIOS Win32** ha queste proprietà.

<dl> <dt>

**BiosCharacteristics**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingString ("Caratteristiche**](/windows/desktop/WmiSdk/standard-qualifiers) BIOS di tipo SMBIOS \| \| 0")
</dt> </dl>

Matrice di caratteristiche BIOS supportate dal sistema in base a quanto definito dalla specifica di riferimento del BIOS di gestione del sistema.

Questo valore proviene dal membro **BioS Characteristics** della struttura di informazioni **BIOS** nelle informazioni SMBIOS.

I valori possibili sono .

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (0)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Caratteristiche BIOS non supportate** (3)


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA è supportato** (4)


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**McA è supportato** (5)


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA è supportato** (6)


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI è supportato** (7)


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) è supportato** (8)


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play supportato** (9)


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM è supportato** (10)


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS aggiornabile (Flash)** (11)


</dt> <dd>

BIOS è aggiornabile (Flash)

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**Lo shadowing BIOS è consentito** (12)


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA è supportato** (13)


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**È disponibile il supporto ESCD** (14)


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**L'avvio da CD è supportato** (15)


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**L'avvio selezionabile è supportato** (16)


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM è socketed** (17)


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Avvio da PC Card (PCMCIA) è supportato** (18)


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**La specifica EDD (Enhanced Disk Drive) è supportata** (19)


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Floppy giapponese per NEC 9800 1,2 mb (3,5 \\ ", 1 kb byte/settore, 360 RPM)** è supportato (20)


</dt> <dd>

Int 13h - Floppy giapponese per NEC 9800 1,2 mb (3,5, 1.000 byte/settore, 360 RPM) è supportato

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Floppy giapponese per Toshiba 1,2 mb (3,5 \\ ", 360 RPM)** è supportato (21)


</dt> <dd>

Int 13h - Floppy giapponese per Toshiba 1,2 mb (3,5, 360 RPM) è supportato

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5,25 \\ " / 360 KB Sono** supportati i servizi Floppy (22)


</dt> <dd>

Sono supportati i servizi Floppy int 13h - 5,25/360 KB

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5,25 \\ " /1,2 MB Sono** supportati i servizi Floppy (23)


</dt> <dd>

Int 13h - 5.25 /1.2MB Floppy Services are supported

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3,5 \\ " / 720 KB Sono** supportati i servizi Floppy (24)


</dt> <dd>

Sono supportati i servizi Floppy int 13h - 3,5/720 KB

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3,5 \\ " / 2,88 MB Sono** supportati i servizi Floppy (25)


</dt> <dd>

Int 13h - 3,5 / 2,88 MB Sono supportati i servizi Floppy

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, il servizio print screen è supportato** (26)


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported (27) (Int 9h, 8042 Keyboard services are supported (27) (Int 9h, 8042 Keyboard services are supported** (27)


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, sono supportati i servizi seriali** (28)


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, sono supportati i servizi di stampa** (29)


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, sono supportati i servizi video CGA/Mono** (30)


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supportato** (32)


</dt> <dd>

ACPI è supportato

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**Usb Legacy è supportato** (33)


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP è supportato** (34)


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**L'avvio I2O è supportato** (35)


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**L'avvio LS-120 è supportato** (36)


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**L'avvio dell'unità ZIP ATAPI è supportato** (37)


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**L'avvio 1394 è supportato** (38)


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Batteria intelligente supportata** (39)


</dt> <dd>

La batteria intelligente è supportata

</dd> <dt>

40 47
</dt> <dd>

Riservato al fornitore del BIOS

</dd> <dt>

48 63
</dt> <dd>

Riservato per il fornitore del sistema

</dd> </dl>

</dd> <dt>

**BIOSVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice delle informazioni complete sul BIOS di sistema. In molti computer possono essere presenti diverse stringhe di versione archiviate nel Registro di sistema e che rappresentano le informazioni del BIOS di sistema.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.4")
</dt> </dl>

Identificatore interno per la compilazione di questo elemento software.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto, una stringa di una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Set di codice usato da questo elemento software.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| Current Language")
</dt> </dl>

Nome della lingua BIOS corrente.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**EmbeddedControllerMajorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SmBIOS \| Type 0 Embedded Controller Firmware Major \| Release")
</dt> </dl>

Versione principale del firmware del controller incorporato.

Questo valore deriva dal membro **Embedded Controller Firmware Major Release** della struttura DI INFORMAZIONI **BIOS** nelle informazioni SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.

</dd> <dt>

**EmbeddedControllerMinorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SmBIOS \| Type 0 Embedded Controller Firmware Minor \| Release")
</dt> </dl>

Versione secondaria del firmware del controller incorporato.

Questo valore deriva dal membro **Embedded Controller Firmware Minor Release** della struttura **BIOS Information** nelle informazioni SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.

</dd> <dt>

**Codice di identificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.7")
</dt> </dl>

Identificatore del produttore per questo elemento software. Spesso si tratta di un'unità di mantenimento delle scorte (SKU) o di un numero di parte.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**InstallableLanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Linguaggi installabili di tipo SMBIOS \| 13") \|
</dt> </dl>

Numero di lingue disponibili per l'installazione in questo sistema. La lingua può determinare proprietà quali la necessità di unicode e testo bidirezionale.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.6")
</dt> </dl>

Edizione del linguaggio di questo elemento software. È necessario usare i codici di lingua definiti in ISO 639. Se l'elemento software rappresenta una versione multilingue o internazionale di un prodotto, deve essere usata la stringa "multilingue".

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stringhe del linguaggio di tipo SMBIOS \| 13") \|
</dt> </dl>

Matrice di nomi delle lingue disponibili installabili con BIOS.

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.2")
</dt> </dl>

Produttore di questo elemento software.

Questo valore deriva dal **membro Vendor** della struttura **BIOS Information** nelle informazioni SMBIOS.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome usato per identificare questo elemento software.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Registra il produttore e il tipo di sistema operativo per un elemento software quando il valore della **proprietà TargetOperatingSystem** è 1 (Altro). Quando **TargetOperatingSystem** ha un valore pari a 1, **OtherTargetOS** deve avere un valore diverso da Null. Per tutti gli altri valori **di TargetOperatingSystem**, **OtherTargetOS** è **NULL.**

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. BIOS di sistema DMTF \| \| 001.9")
</dt> </dl>

Se **TRUE,** si tratta del BIOS primario del sistema informatico.

Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](cim-bioselement.md).

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di rilascio del BIOS Windows nel formato Coordinated Universal Time (UTC) di AAAAMMGGHHMMSS. MMMMMM(+-)OOO.

Questo valore deriva dal **membro BIOS Release Date** della struttura **BIOS Information** nelle informazioni SMBIOS.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.4")
</dt> </dl>

Numero di serie assegnato dell'elemento software.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**SMBIOSBIOSBIOSVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Versione BIOS di tipo SMBIOS \| \| 0")
</dt> </dl>

Versione del BIOS segnalata da SMBIOS.

Questo valore deriva dal **membro versione BIOS** della struttura di informazioni **BIOS** nelle informazioni SMBIOS.

</dd> <dt>

**SMBIOSMajorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")
</dt> </dl>

Numero di versione SMBIOS principale. Questa proprietà è **NULL** se SMBIOS non viene trovato.

</dd> <dt>

**SMBIOSMinorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")
</dt> </dl>

Numero di versione SMBIOS secondario. Questa proprietà è **NULL** se SMBIOS non viene trovato.

</dd> <dt>

**SMBIOSPresent**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| Init")
</dt> </dl>

Se **true,** smBIOS è disponibile in questo computer.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](/windows/desktop/WmiSdk/key-qualifier) [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificatore per questo elemento software. progettato per essere utilizzato insieme ad altre chiavi per creare una rappresentazione univoca di questa istanza.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Stato di un elemento software.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

I valori possibili sono .

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

**Distribuibile** (0)


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

**Installable** (1)


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

**Eseguibile** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**In** esecuzione (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono online, ma l'elemento gestito non è "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

I valori possibili sono .

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degraded** ("Degraded")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("Sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** ("Arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("Servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("Nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Lost Comm** ("Lost Comm")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemBiosMajorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 System \| BIOS Major Release")
</dt> </dl>

Versione principale del BIOS di sistema.

Questo valore proviene dal membro **versione principale del BIOS** di sistema della struttura di **informazioni BIOS** nelle informazioni SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.

</dd> <dt>

**SystemBiosMinorVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 System \| BIOS Minor Release")
</dt> </dl>

Versione secondaria del BIOS di sistema.

Questo valore proviene dal membro **versione secondaria del BIOS** di sistema della struttura di **informazioni BIOS** nelle informazioni SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](/windows/desktop/WmiSdk/key-qualifier) [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Sistema operativo di destinazione dell'elemento software proprietario.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

I valori possibili sono .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

**MACOS** (2)


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

**Digital Unix** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

**Sistema operativo/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

**WINCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

**Sequenziante** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

**IRIX** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

**Solaris** (29)


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

**GNU Hurd** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

**Kernel MACH** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

**Ilva** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

**NextStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**Dedicato** (59)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

**VSE** (60)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

**TPF** (61)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HARDWARE Description \\ \\ \\ \\ \| SystemBiosVersion")
</dt> </dl>

Versione del BIOS. Questa stringa viene creata dal produttore del BIOS.

Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ BIOS Win32** è derivata da [**CIM \_ BIOSElement.**](cim-bioselement.md)

Le proprietà nella classe **\_ BIOS Win32** possono cambiare per un computer specifico con lo stesso BIOS, ad esempio l'avvio tramite una modalità BIOS legacy o l'avvio tramite la modalità BIOS UEFI. Tuttavia, le proprietà recuperate dalle strutture SMBIOS devono rimanere invariate.

## <a name="examples"></a>Esempio

L'esempio [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI) PowerShell (Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in TechNet Gallery usa una serie di chiamate all'hardware e al software, incluso **il \_ BIOS Win32,** per visualizzare informazioni su un sistema locale o remoto.

L'esempio VBScript Generate system information as XML hierarchy (Genera informazioni di sistema come gerarchia [XML)](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) in TechNet Gallery usa una serie di chiamate all'hardware e al software, incluso il **\_ BIOS Win32,** per generare una rappresentazione XML di un sistema usando un output XML manuale.

L'esempio di codice di PowerShell seguente usa **il \_ BIOS Win32** per restituire le caratteristiche del BIOS


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



L'esempio di codice precedente restituisce le informazioni seguenti:

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

