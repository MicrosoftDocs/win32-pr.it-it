---
description: La \_ classe WMI PortConnector Win32 rappresenta le porte di connessione fisiche, ad esempio DB-25 pin maschio, Centronics o PS/2.
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Classe Win32_PortConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225543"
---
# <a name="win32_portconnector-class"></a>Win32 \_ PortConnector (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortConnector Win32** rappresenta le porte di connessione fisiche, ad esempio DB-25 pin maschio, Centronics o PS/2.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PortConnector** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PortConnector** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione dell'oggetto, ovvero una stringa a una riga.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Aggiungere la configurazione e l'utilizzo dei segnali di un connettore fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).

</dd> <dt>

**ConnectorType**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 8 \| connettore interno/esterno")
</dt> </dl>

Matrice di attributi fisici del connettore utilizzato da questa porta.

Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md). Nell'elenco seguente sono elencati i valori.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>**Maschio** (2)


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Schermato** (4)


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>Non **schermato** (5)


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pin)** (6)


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pin)** (7)


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**High-Density SCSI (P) (68 pin)** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pin)** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pin)** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Fibre Channel SCSI (DB-9, rame)** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**Fibre Channel SCSI (fibre)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pin)** (13)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pin)** (14)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 pollice (40 pin)** (16)


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 inch (44 pin)** (17)


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span id="v.35"></span>**V. 35** (30)


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span id="x.21"></span>**X. 21** (31)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span id="AUI"></span><span id="aui"></span>**AUI** (33)


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**Categoria UTP 3** (34)


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP categoria 4** (35)


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**Categoria UTP 5** (36)


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span id="BNC"></span><span id="bnc"></span>**BNC** (37)


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span id="PCI"></span><span id="pci"></span>**PCI** (43)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span id="ISA"></span><span id="isa"></span>**ISA** (44)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span id="EISA"></span><span id="eisa"></span>**EISA** (45)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span id="VESA"></span><span id="vesa"></span>**VESA** (46)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**Tipi PCMCIA I** (48)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**Tipo PCMCIA II** (49)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**Tipo PCMCIA III** (50)


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Porta ZV** (51)


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span id="USB"></span><span id="usb"></span>**USB** (53)


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pin)** (56)


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span id="DIN"></span><span id="din"></span>**DIN** (58)


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (62)


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span id="HP-HIL"></span><span id="hp-hil"></span>**HP-** b (63)


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. bus** (64)


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**Nubus** (65)


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Tipo Mini-Centronics-14** (68)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Tipo Mini-Centronics-20** (69)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Tipo Mini-Centronics-26** (70)


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Mouse bus** (71)


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span id="ADB"></span><span id="adb"></span>**ADB** (72)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span id="AGP"></span><span id="agp"></span>**AGP** (73)


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Bus VME** (74)


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span id="VME64"></span><span id="vme64"></span>**VME64** (75)


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietario** (76)


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Slot scheda processore proprietario** (77)


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Slot scheda di memoria proprietaria** (78)


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Slot di riser I/O proprietario** (79)


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)


</dt> <dd>

PC-98-Hireso

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-jack** (88)


</dt> <dd>

SCSI SSA

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Floppy su lavagna** (89)


</dt> <dd>

Circolare

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**6 pin dual inline (pin 10 Cut)** (90)


</dt> <dd>

Connettore IDE a bordo

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 pin dual inline (pin 26 Cut)** (91)


</dt> <dd>

Connettore floppy a bordo

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**Pin 50 dual inline** (92)


</dt> <dd>

2 pin doppio inline

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**Pin 68 dual inline** (93)


</dt> <dd>

25 pin doppio inline

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Input audio su lavagna da CD-ROM** (94)


</dt> <dd>

Pin 50 dual inline

</dd> <dt>

95
</dt> <dd>

Pin 68 dual inline

</dd> <dt>

96
</dt> <dd>

Connettore audio a bordo

</dd> <dt>

97
</dt> <dd>

Mini-Jack

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

SBus IEEE 1396-1993 32 bit

</dd> <dt>

100
</dt> <dd>

SBus IEEE 1396-1993 64 bit

</dd> <dt>

101
</dt> <dd>

Contratto del cliente Microsoft

</dd> <dt>

102
</dt> <dd>

GIO

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

HIO

</dd> <dt>

105
</dt> <dd>

NGIO

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

MTRJ

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

I/O futuro

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Electrical

</dd> <dt>

113
</dt> <dd>

Ottico

</dd> <dt>

114
</dt> <dd>

Barra multifunzione

</dd> <dt>

115
</dt> <dd>

GLM

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Mini SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

HSSC

</dd> <dt>

120
</dt> <dd>

Schermate VHDCI (68 pin)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza. Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ExternalReferenceDesignator**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 8 \| External Reference Designator")
</dt> </dl>

Indicatore di riferimento esterno della porta. Gli designatori di riferimento esterno sono identificatori che determinano il tipo e l'utilizzo della porta.

Esempio: "COM1"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InternalReferenceDesignator**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 8 \| Internal Reference Designator")
</dt> </dl>

Indicatore di riferimento interno della porta. Gli designatori di riferimento interni sono specifici del produttore e identificano la posizione della lavagna o l'utilizzo della porta.

Esempio: "J101"

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome dell'organizzazione responsabile della creazione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Modello**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Nome dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta per l'oggetto. Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico. Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset. Se solo i dati del codice a barre sono disponibili e sono univoci oppure possono essere utilizzati come chiave di elemento, questa proprietà è **null** e i dati del codice a barre vengono utilizzati come chiave della classe nella proprietà Tag.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**NumeroArticolo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo di \| porta 8")
</dt> </dl>

Funzione della porta. Nell'elenco seguente sono elencati i valori.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

**Porta parallela XT/AT compatibile** (1)


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

**Porta parallela PS/2** (2)


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

**Porta parallela ECP** (3)


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

**Porta Parallela EPP** (4)


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

**Porta parallela ECP/EPP** (5)


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

**Porta seriale XT/AT Compatible** (6)


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

**Porta seriale compatibile 16450** (7)


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

**Porta seriale 16550 compatibile** (8)


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

**Compatibile con la porta seriale 16550A** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

**Porta SCSI** (10)


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

**Porta MIDI** (11)


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

**Porta Joy Stick** (12)


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

**Porta tastiera** (13)


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

**Porta del mouse** (14)


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

**SCSI ssa** (15)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (16)


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

**FireWire (IEEE P1394)** (17)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

**Tipo PCMCIA II** (18)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

**Tipo PCMCIA II** (19)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

**Tipo PCMCIA III** (20)


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

**CardBus** (21)


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

**Porta bus di accesso** (22)


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

**SCSI II** (23)


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

**SCSI Wide** (24)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (25)


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

**PC-98-Hireso** (26)


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

**PC-H98** (27)


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

**Porta video** (28)


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

**Porta audio** (29)


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

**Porta modem** (30)


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

**Porta di rete** (31)


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**8251 compatibile** (32)


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

**8251 compatibile con FIFO** (33)


</dt> <dd></dd> </dl>

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'elemento fisico è acceso.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numero allocato dal produttore utilizzato per identificare un elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Numero di unità di conservazione per un elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificatore univoco di una connessione porta nel computer.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

Esempio: "Port Connector 1"

</dd> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Versione dell'elemento fisico.

Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PortConnector** è derivata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
