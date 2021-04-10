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
# <a name="win32_portconnector-class"></a><span data-ttu-id="aa9fc-103">Win32 \_ PortConnector (classe)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="aa9fc-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortConnector Win32** rappresenta le porte di connessione fisiche, ad esempio DB-25 pin maschio, Centronics o PS/2.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="aa9fc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aa9fc-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9fc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa9fc-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="aa9fc-108">Members</span><span class="sxs-lookup"><span data-stu-id="aa9fc-108">Members</span></span>

<span data-ttu-id="aa9fc-109">La classe **Win32 \_ PortConnector** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aa9fc-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="aa9fc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aa9fc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa9fc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="aa9fc-111">Properties</span></span>

<span data-ttu-id="aa9fc-112">La classe **Win32 \_ PortConnector** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa9fc-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-116">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-117">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="aa9fc-118">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-119">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-122">Aggiungere la configurazione e l'utilizzo dei segnali di un connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="aa9fc-123">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-124">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-125">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-127">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 8 \| connettore interno/esterno")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-128">Matrice di attributi fisici del connettore utilizzato da questa porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="aa9fc-129">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="aa9fc-130">Nell'elenco seguente sono elencati i valori.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa9fc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa9fc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="aa9fc-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Maschio** (2)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="aa9fc-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="aa9fc-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Schermato** (4)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="aa9fc-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>Non **schermato** (5)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="aa9fc-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pin)** (6)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="aa9fc-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="aa9fc-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**High-Density SCSI (P) (68 pin)** (8)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="aa9fc-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pin)** (9)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="aa9fc-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pin)** (10)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="aa9fc-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Fibre Channel SCSI (DB-9, rame)** (11)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="aa9fc-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="aa9fc-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pin)** (13)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="aa9fc-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pin)** (14)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="aa9fc-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="aa9fc-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 pollice (40 pin)** (16)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="aa9fc-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 inch (44 pin)** (17)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="aa9fc-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="aa9fc-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="aa9fc-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="aa9fc-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="aa9fc-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="aa9fc-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="aa9fc-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="aa9fc-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="aa9fc-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="aa9fc-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="aa9fc-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="aa9fc-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="aa9fc-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="aa9fc-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="aa9fc-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="aa9fc-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="aa9fc-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**Categoria UTP 3** (34)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="aa9fc-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="aa9fc-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**Categoria UTP 5** (36)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="aa9fc-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="aa9fc-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="aa9fc-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="aa9fc-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="aa9fc-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="aa9fc-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="aa9fc-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="aa9fc-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="aa9fc-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="aa9fc-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="aa9fc-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="aa9fc-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**Tipi PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="aa9fc-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**Tipo PCMCIA II** (49)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="aa9fc-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**Tipo PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="aa9fc-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="aa9fc-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="aa9fc-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="aa9fc-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="aa9fc-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="aa9fc-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pin)** (56)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="aa9fc-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="aa9fc-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="aa9fc-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="aa9fc-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="aa9fc-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="aa9fc-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (62)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="aa9fc-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-** b (63)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="aa9fc-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="aa9fc-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="aa9fc-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="aa9fc-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="aa9fc-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Tipo Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="aa9fc-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Tipo Mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="aa9fc-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Tipo Mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="aa9fc-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Mouse bus** (71)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="aa9fc-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="aa9fc-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="aa9fc-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="aa9fc-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="aa9fc-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietario** (76)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="aa9fc-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Slot scheda processore proprietario** (77)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="aa9fc-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Slot scheda di memoria proprietaria** (78)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="aa9fc-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Slot di riser I/O proprietario** (79)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="aa9fc-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="aa9fc-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="aa9fc-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="aa9fc-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="aa9fc-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-216">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="aa9fc-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="aa9fc-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="aa9fc-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="aa9fc-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="aa9fc-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-jack** (88)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-221">SCSI SSA</span><span class="sxs-lookup"><span data-stu-id="aa9fc-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="aa9fc-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Floppy su lavagna** (89)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-223">Circolare</span><span class="sxs-lookup"><span data-stu-id="aa9fc-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="aa9fc-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**6 pin dual inline (pin 10 Cut)** (90)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-225">Connettore IDE a bordo</span><span class="sxs-lookup"><span data-stu-id="aa9fc-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="aa9fc-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 pin dual inline (pin 26 Cut)** (91)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-227">Connettore floppy a bordo</span><span class="sxs-lookup"><span data-stu-id="aa9fc-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="aa9fc-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**Pin 50 dual inline** (92)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-229">2 pin doppio inline</span><span class="sxs-lookup"><span data-stu-id="aa9fc-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="aa9fc-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**Pin 68 dual inline** (93)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-231">25 pin doppio inline</span><span class="sxs-lookup"><span data-stu-id="aa9fc-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="aa9fc-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Input audio su lavagna da CD-ROM** (94)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="aa9fc-233">Pin 50 dual inline</span><span class="sxs-lookup"><span data-stu-id="aa9fc-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-234">95</span><span class="sxs-lookup"><span data-stu-id="aa9fc-234">95</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-235">Pin 68 dual inline</span><span class="sxs-lookup"><span data-stu-id="aa9fc-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-236">96</span><span class="sxs-lookup"><span data-stu-id="aa9fc-236">96</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-237">Connettore audio a bordo</span><span class="sxs-lookup"><span data-stu-id="aa9fc-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-238">97</span><span class="sxs-lookup"><span data-stu-id="aa9fc-238">97</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="aa9fc-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-240">98</span><span class="sxs-lookup"><span data-stu-id="aa9fc-240">98</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="aa9fc-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-242">99</span><span class="sxs-lookup"><span data-stu-id="aa9fc-242">99</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-243">SBus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="aa9fc-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-244">100</span><span class="sxs-lookup"><span data-stu-id="aa9fc-244">100</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-245">SBus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="aa9fc-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-246">101</span><span class="sxs-lookup"><span data-stu-id="aa9fc-246">101</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-247">Contratto del cliente Microsoft</span><span class="sxs-lookup"><span data-stu-id="aa9fc-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-248">102</span><span class="sxs-lookup"><span data-stu-id="aa9fc-248">102</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-249">GIO</span><span class="sxs-lookup"><span data-stu-id="aa9fc-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-250">103</span><span class="sxs-lookup"><span data-stu-id="aa9fc-250">103</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-251">XIO</span><span class="sxs-lookup"><span data-stu-id="aa9fc-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-252">104</span><span class="sxs-lookup"><span data-stu-id="aa9fc-252">104</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-253">HIO</span><span class="sxs-lookup"><span data-stu-id="aa9fc-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-254">105</span><span class="sxs-lookup"><span data-stu-id="aa9fc-254">105</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-255">NGIO</span><span class="sxs-lookup"><span data-stu-id="aa9fc-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-256">106</span><span class="sxs-lookup"><span data-stu-id="aa9fc-256">106</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-257">PMC</span><span class="sxs-lookup"><span data-stu-id="aa9fc-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-258">107</span><span class="sxs-lookup"><span data-stu-id="aa9fc-258">107</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="aa9fc-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-260">108</span><span class="sxs-lookup"><span data-stu-id="aa9fc-260">108</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="aa9fc-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-262">109</span><span class="sxs-lookup"><span data-stu-id="aa9fc-262">109</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-263">I/O futuro</span><span class="sxs-lookup"><span data-stu-id="aa9fc-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-264">110</span><span class="sxs-lookup"><span data-stu-id="aa9fc-264">110</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-265">SC</span><span class="sxs-lookup"><span data-stu-id="aa9fc-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-266">111</span><span class="sxs-lookup"><span data-stu-id="aa9fc-266">111</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-267">SG</span><span class="sxs-lookup"><span data-stu-id="aa9fc-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-268">112</span><span class="sxs-lookup"><span data-stu-id="aa9fc-268">112</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-269">Electrical</span><span class="sxs-lookup"><span data-stu-id="aa9fc-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-270">113</span><span class="sxs-lookup"><span data-stu-id="aa9fc-270">113</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-271">Ottico</span><span class="sxs-lookup"><span data-stu-id="aa9fc-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-272">114</span><span class="sxs-lookup"><span data-stu-id="aa9fc-272">114</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-273">Barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="aa9fc-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-274">115</span><span class="sxs-lookup"><span data-stu-id="aa9fc-274">115</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-275">GLM</span><span class="sxs-lookup"><span data-stu-id="aa9fc-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-276">116</span><span class="sxs-lookup"><span data-stu-id="aa9fc-276">116</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-277">1x9</span><span class="sxs-lookup"><span data-stu-id="aa9fc-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-278">117</span><span class="sxs-lookup"><span data-stu-id="aa9fc-278">117</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-279">Mini SG</span><span class="sxs-lookup"><span data-stu-id="aa9fc-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-280">118</span><span class="sxs-lookup"><span data-stu-id="aa9fc-280">118</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-281">LC</span><span class="sxs-lookup"><span data-stu-id="aa9fc-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-282">119</span><span class="sxs-lookup"><span data-stu-id="aa9fc-282">119</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="aa9fc-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-284">120</span><span class="sxs-lookup"><span data-stu-id="aa9fc-284">120</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-285">Schermate VHDCI (68 pin)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-286">121</span><span class="sxs-lookup"><span data-stu-id="aa9fc-286">121</span></span>
</dt> <dd>

<span data-ttu-id="aa9fc-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="aa9fc-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa9fc-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-291">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-292">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="aa9fc-293">Se utilizzata con le altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="aa9fc-294">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-295">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-296">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-298">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-299">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-299">Description of the object.</span></span>

<span data-ttu-id="aa9fc-300">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-304">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 8 \| External Reference Designator")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-305">Indicatore di riferimento esterno della porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-305">External reference designator of the port.</span></span> <span data-ttu-id="aa9fc-306">Gli designatori di riferimento esterno sono identificatori che determinano il tipo e l'utilizzo della porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="aa9fc-307">Esempio: "COM1"</span><span class="sxs-lookup"><span data-stu-id="aa9fc-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-309">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-311">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-312">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-312">Date and time the object is installed.</span></span> <span data-ttu-id="aa9fc-313">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aa9fc-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-315">**InternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-318">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 8 \| Internal Reference Designator")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-319">Indicatore di riferimento interno della porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-319">Internal reference designator of the port.</span></span> <span data-ttu-id="aa9fc-320">Gli designatori di riferimento interni sono specifici del produttore e identificano la posizione della lavagna o l'utilizzo della porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="aa9fc-321">Esempio: "J101"</span><span class="sxs-lookup"><span data-stu-id="aa9fc-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-322">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-323">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-325">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-326">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="aa9fc-327">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-328">**Modello**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-329">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-330">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-331">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-332">Nome dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-332">Name for the physical element.</span></span>

<span data-ttu-id="aa9fc-333">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-334">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-335">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-337">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-338">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-338">Label for the object.</span></span> <span data-ttu-id="aa9fc-339">Quando è sottoclassata, è possibile eseguire l'override della proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="aa9fc-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-344">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="aa9fc-345">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="aa9fc-346">Se solo i dati del codice a barre sono disponibili e sono univoci oppure possono essere utilizzati come chiave di elemento, questa proprietà è **null** e i dati del codice a barre vengono utilizzati come chiave della classe nella proprietà Tag.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="aa9fc-347">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-348">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-349">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-351">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-352">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="aa9fc-353">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-355">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-357">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo di \| porta 8")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-358">Funzione della porta.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-358">Function of the port.</span></span> <span data-ttu-id="aa9fc-359">Nell'elenco seguente sono elencati i valori.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="aa9fc-360">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-361">**Porta parallela XT/AT compatibile** (1)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="aa9fc-362">**Porta parallela PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="aa9fc-363">**Porta parallela ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="aa9fc-364">**Porta Parallela EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="aa9fc-365">**Porta parallela ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-366">**Porta seriale XT/AT Compatible** (6)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-367">**Porta seriale compatibile 16450** (7)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-368">**Porta seriale 16550 compatibile** (8)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-369">**Compatibile con la porta seriale 16550A** (9)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="aa9fc-370">**Porta SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="aa9fc-371">**Porta MIDI** (11)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="aa9fc-372">**Porta Joy Stick** (12)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="aa9fc-373">**Porta tastiera** (13)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="aa9fc-374">**Porta del mouse** (14)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="aa9fc-375">**SCSI ssa** (15)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="aa9fc-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="aa9fc-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="aa9fc-378">**Tipo PCMCIA II** (18)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="aa9fc-379">**Tipo PCMCIA II** (19)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="aa9fc-380">**Tipo PCMCIA III** (20)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="aa9fc-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="aa9fc-382">**Porta bus di accesso** (22)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="aa9fc-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="aa9fc-384">**SCSI Wide** (24)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="aa9fc-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="aa9fc-386">**PC-98-Hireso** (26)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="aa9fc-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="aa9fc-388">**Porta video** (28)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="aa9fc-389">**Porta audio** (29)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="aa9fc-390">**Porta modem** (30)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="aa9fc-391">**Porta di rete** (31)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-392">**8251 compatibile** (32)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="aa9fc-393">**8251 compatibile con FIFO** (33)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa9fc-394">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-395">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-397">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="aa9fc-398">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-400">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-402">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-403">Numero allocato dal produttore utilizzato per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="aa9fc-404">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-408">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-409">Numero di unità di conservazione per un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="aa9fc-410">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-411">**Status**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-414">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-415">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-415">Current status of the object.</span></span> <span data-ttu-id="aa9fc-416">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aa9fc-417">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aa9fc-418">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="aa9fc-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aa9fc-419">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aa9fc-420">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aa9fc-421">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aa9fc-422">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa9fc-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aa9fc-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aa9fc-424">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa9fc-425">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="aa9fc-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa9fc-426">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aa9fc-427">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aa9fc-428">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aa9fc-429">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aa9fc-430">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aa9fc-431">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aa9fc-432">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aa9fc-433">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aa9fc-434">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa9fc-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-438">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="aa9fc-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-439">Identificatore univoco di una connessione porta nel computer.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="aa9fc-440">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="aa9fc-441">Esempio: "Port Connector 1"</span><span class="sxs-lookup"><span data-stu-id="aa9fc-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="aa9fc-442">**Versione**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa9fc-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="aa9fc-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa9fc-445">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="aa9fc-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aa9fc-446">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="aa9fc-446">Version of the physical element.</span></span>

<span data-ttu-id="aa9fc-447">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa9fc-448">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa9fc-448">Remarks</span></span>

<span data-ttu-id="aa9fc-449">La classe **Win32 \_ PortConnector** è derivata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="aa9fc-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9fc-450">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa9fc-450">Requirements</span></span>



| <span data-ttu-id="aa9fc-451">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa9fc-451">Requirement</span></span> | <span data-ttu-id="aa9fc-452">Valore</span><span class="sxs-lookup"><span data-stu-id="aa9fc-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9fc-453">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa9fc-453">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9fc-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa9fc-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa9fc-455">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa9fc-455">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9fc-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa9fc-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa9fc-457">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa9fc-457">Namespace</span></span><br/>                | <span data-ttu-id="aa9fc-458">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="aa9fc-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa9fc-459">MOF</span><span class="sxs-lookup"><span data-stu-id="aa9fc-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa9fc-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa9fc-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa9fc-461">DLL</span><span class="sxs-lookup"><span data-stu-id="aa9fc-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9fc-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9fc-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9fc-463">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa9fc-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9fc-464">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="aa9fc-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="aa9fc-465">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="aa9fc-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
