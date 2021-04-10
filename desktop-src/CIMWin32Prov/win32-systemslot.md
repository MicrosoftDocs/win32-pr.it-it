---
description: Win32 \_ SystemSlot &\# 32; La classe WMI rappresenta punti di connessione fisici, tra cui porte, slot della scheda madre e periferiche e punti di connessione proprietari.
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Classe Win32_SystemSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127594"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="544cc-103">Win32 \_ SystemSlot (classe)</span><span class="sxs-lookup"><span data-stu-id="544cc-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="544cc-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSlot Win32** rappresenta punti di connessione fisici, tra cui porte, slot della scheda madre e periferiche e punti di connessione proprietari.</span><span class="sxs-lookup"><span data-stu-id="544cc-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="544cc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="544cc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="544cc-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="544cc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="544cc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="544cc-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="544cc-108">Members</span><span class="sxs-lookup"><span data-stu-id="544cc-108">Members</span></span>

<span data-ttu-id="544cc-109">La classe **Win32 \_ SystemSlot** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="544cc-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="544cc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="544cc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="544cc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="544cc-111">Properties</span></span>

<span data-ttu-id="544cc-112">La classe **Win32 \_ SystemSlot** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="544cc-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="544cc-113">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="544cc-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="544cc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-116">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 9 \| bus number")</span><span class="sxs-lookup"><span data-stu-id="544cc-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-117">Numero del bus di SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="544cc-118">Questo valore deriva dal membro **bus number** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-119">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="544cc-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-120">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="544cc-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-123">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="544cc-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-124">Breve descrizione di un oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="544cc-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="544cc-125">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-126">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="544cc-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="544cc-129">Stringa in formato libero che descrive la configurazione del PIN e l'utilizzo del segnale di un connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="544cc-130">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-131">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="544cc-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-132">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="544cc-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-134">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo di slot di tipo 9 SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="544cc-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-135">Matrice di attributi fisici del connettore usato da questo slot.</span><span class="sxs-lookup"><span data-stu-id="544cc-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="544cc-136">Questo valore deriva dal membro di **tipo slot** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-137">Questa proprietà viene ereditata da [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="544cc-138">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="544cc-139">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="544cc-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="544cc-140">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="544cc-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="544cc-141">**Maschio** (2)</span><span class="sxs-lookup"><span data-stu-id="544cc-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="544cc-142">**Female** (3)</span><span class="sxs-lookup"><span data-stu-id="544cc-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="544cc-143">**Schermato** (4)</span><span class="sxs-lookup"><span data-stu-id="544cc-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="544cc-144">Non **schermato** (5)</span><span class="sxs-lookup"><span data-stu-id="544cc-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="544cc-145">**SCSI (A) High-Density (50 pin)** (6)</span><span class="sxs-lookup"><span data-stu-id="544cc-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="544cc-146">**SCSI (A) Low-Density (50 pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="544cc-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="544cc-147">**High-Density SCSI (P) (68 pin)** (8)</span><span class="sxs-lookup"><span data-stu-id="544cc-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="544cc-148">**SCSI SCA-I (80 pin)** (9)</span><span class="sxs-lookup"><span data-stu-id="544cc-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="544cc-149">**SCSI SCA-II (80 pin)** (10)</span><span class="sxs-lookup"><span data-stu-id="544cc-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="544cc-150">**Fibre Channel SCSI (DB-9, rame)** (11)</span><span class="sxs-lookup"><span data-stu-id="544cc-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="544cc-151">**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="544cc-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="544cc-152">**SCSI Fibre Channel SCA-II (40 pin)** (13)</span><span class="sxs-lookup"><span data-stu-id="544cc-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="544cc-153">**SCSI Fibre Channel SCA-II (20 pin)** (14)</span><span class="sxs-lookup"><span data-stu-id="544cc-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="544cc-154">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="544cc-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="544cc-155">**ATA 3-1/2 pollice (40 pin)** (16)</span><span class="sxs-lookup"><span data-stu-id="544cc-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="544cc-156">**ATA 2-1/2 inch (44 pin)** (17)</span><span class="sxs-lookup"><span data-stu-id="544cc-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="544cc-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="544cc-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="544cc-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="544cc-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="544cc-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="544cc-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="544cc-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="544cc-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="544cc-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="544cc-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="544cc-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="544cc-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="544cc-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="544cc-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="544cc-164">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="544cc-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="544cc-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="544cc-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="544cc-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="544cc-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="544cc-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="544cc-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="544cc-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="544cc-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="544cc-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="544cc-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="544cc-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="544cc-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="544cc-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="544cc-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="544cc-172">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="544cc-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="544cc-173">**Categoria UTP 3** (34)</span><span class="sxs-lookup"><span data-stu-id="544cc-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="544cc-174">**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="544cc-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="544cc-175">**Categoria UTP 5** (36)</span><span class="sxs-lookup"><span data-stu-id="544cc-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="544cc-176">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="544cc-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="544cc-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="544cc-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="544cc-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="544cc-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="544cc-179">**Fiber MIC** (40)</span><span class="sxs-lookup"><span data-stu-id="544cc-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="544cc-180">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="544cc-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="544cc-181">**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="544cc-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="544cc-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="544cc-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="544cc-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="544cc-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="544cc-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="544cc-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="544cc-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="544cc-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="544cc-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="544cc-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="544cc-187">**Tipi PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="544cc-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="544cc-188">**Tipo PCMCIA II** (49)</span><span class="sxs-lookup"><span data-stu-id="544cc-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="544cc-189">**Tipo PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="544cc-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="544cc-190">**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="544cc-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="544cc-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="544cc-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="544cc-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="544cc-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="544cc-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="544cc-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="544cc-194">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="544cc-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="544cc-195">**HSSDC (6 pin)** (56)</span><span class="sxs-lookup"><span data-stu-id="544cc-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="544cc-196">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="544cc-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="544cc-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="544cc-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="544cc-198">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="544cc-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="544cc-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="544cc-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="544cc-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="544cc-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="544cc-201">**Infrarossi** (62)</span><span class="sxs-lookup"><span data-stu-id="544cc-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="544cc-202">**HP-** b (63)</span><span class="sxs-lookup"><span data-stu-id="544cc-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="544cc-203">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="544cc-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="544cc-204">**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="544cc-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="544cc-205">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="544cc-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="544cc-206">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="544cc-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="544cc-207">**Tipo Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="544cc-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="544cc-208">**Tipo Mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="544cc-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="544cc-209">**Tipo Mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="544cc-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="544cc-210">**Mouse bus** (71)</span><span class="sxs-lookup"><span data-stu-id="544cc-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="544cc-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="544cc-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="544cc-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="544cc-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="544cc-213">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="544cc-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="544cc-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="544cc-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="544cc-215">**Proprietario** (76)</span><span class="sxs-lookup"><span data-stu-id="544cc-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="544cc-216">**Slot scheda processore proprietario** (77)</span><span class="sxs-lookup"><span data-stu-id="544cc-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="544cc-217">**Slot scheda di memoria proprietaria** (78)</span><span class="sxs-lookup"><span data-stu-id="544cc-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="544cc-218">**Slot di riser I/O proprietario** (79)</span><span class="sxs-lookup"><span data-stu-id="544cc-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="544cc-219">**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="544cc-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="544cc-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="544cc-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="544cc-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="544cc-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="544cc-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="544cc-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="544cc-223">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="544cc-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="544cc-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="544cc-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="544cc-225">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="544cc-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="544cc-226">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="544cc-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="544cc-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="544cc-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="544cc-228">**SBus IEEE 1396-1993 32 bit** (89)</span><span class="sxs-lookup"><span data-stu-id="544cc-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="544cc-229">**SBus IEEE 1396-1993 64 bit** (90)</span><span class="sxs-lookup"><span data-stu-id="544cc-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="544cc-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="544cc-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="544cc-231">**Gio** (92)</span><span class="sxs-lookup"><span data-stu-id="544cc-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="544cc-232">**XIO** (93)</span><span class="sxs-lookup"><span data-stu-id="544cc-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="544cc-233">**Hio** (94)</span><span class="sxs-lookup"><span data-stu-id="544cc-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="544cc-234">**NGIO** (95)</span><span class="sxs-lookup"><span data-stu-id="544cc-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="544cc-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="544cc-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="544cc-236">**I/O futuro** (97)</span><span class="sxs-lookup"><span data-stu-id="544cc-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="544cc-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="544cc-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="544cc-238">**AGP8X** (99)</span><span class="sxs-lookup"><span data-stu-id="544cc-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="544cc-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="544cc-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="544cc-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="544cc-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-243">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="544cc-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-244">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="544cc-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="544cc-245">Se utilizzata con le altre proprietà chiave di una classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="544cc-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="544cc-246">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="544cc-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-248">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-250">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 9 \| Current Usage")</span><span class="sxs-lookup"><span data-stu-id="544cc-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-251">Stato di utilizzo dello slot di sistema.</span><span class="sxs-lookup"><span data-stu-id="544cc-251">Status of system slot use.</span></span>

<span data-ttu-id="544cc-252">Questo valore deriva dal membro di **utilizzo corrente** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-253">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="544cc-254">**Riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="544cc-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="544cc-255">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="544cc-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="544cc-256">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="544cc-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="544cc-257">**Disponibile** (3)</span><span class="sxs-lookup"><span data-stu-id="544cc-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="544cc-258">**In uso** (4)</span><span class="sxs-lookup"><span data-stu-id="544cc-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="544cc-259">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="544cc-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-262">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="544cc-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-263">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="544cc-263">Description of the object.</span></span>

<span data-ttu-id="544cc-264">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-265">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="544cc-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-266">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="544cc-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-268">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 9 \| dispositivo numero")</span><span class="sxs-lookup"><span data-stu-id="544cc-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-269">Numero del dispositivo SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="544cc-270">Questo valore deriva dal membro del **numero di dispositivo/funzione** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-271">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="544cc-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-272">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="544cc-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="544cc-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-275">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| Function Number")</span><span class="sxs-lookup"><span data-stu-id="544cc-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-276">Numero della funzione SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="544cc-277">Questo valore deriva dal membro del **numero di dispositivo/funzione** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-278">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="544cc-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-279">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="544cc-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-280">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="544cc-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-282">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="544cc-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-283">Altezza massima di una scheda di scheda che può essere inserita nello slot, in pollici.</span><span class="sxs-lookup"><span data-stu-id="544cc-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="544cc-284">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="544cc-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-286">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="544cc-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-288">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="544cc-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-289">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="544cc-289">Date and time the object is installed.</span></span> <span data-ttu-id="544cc-290">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="544cc-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="544cc-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-292">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="544cc-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-293">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="544cc-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-295">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="544cc-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-296">Lunghezza massima di una scheda di scheda che può essere inserita nello slot, in pollici.</span><span class="sxs-lookup"><span data-stu-id="544cc-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="544cc-297">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-298">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="544cc-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-301">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="544cc-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-302">Nome dell'organizzazione che produce l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="544cc-303">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="544cc-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-305">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-307">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| System Slot \| 004,3 "), [**unità**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="544cc-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-308">Larghezza massima del bus delle schede di scheda che possono essere inserite in questo slot, in bit.</span><span class="sxs-lookup"><span data-stu-id="544cc-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="544cc-309">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="544cc-309">This can be one of the following values.</span></span>

<span data-ttu-id="544cc-310">Questo valore deriva dal membro della **larghezza del bus di dati dello slot** della struttura degli slot di **sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-311">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="544cc-312">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="544cc-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="544cc-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="544cc-314">Larghezza massima dati (bit): 8</span><span class="sxs-lookup"><span data-stu-id="544cc-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="544cc-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="544cc-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="544cc-316">Larghezza dati massima (bit): 16</span><span class="sxs-lookup"><span data-stu-id="544cc-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="544cc-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="544cc-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="544cc-318">Larghezza dati massima (bit): 32</span><span class="sxs-lookup"><span data-stu-id="544cc-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="544cc-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="544cc-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="544cc-320">Larghezza dati massima (bit): 64</span><span class="sxs-lookup"><span data-stu-id="544cc-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="544cc-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="544cc-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="544cc-322">Larghezza dati massima (bit): 128</span><span class="sxs-lookup"><span data-stu-id="544cc-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="544cc-323">**Modello**</span><span class="sxs-lookup"><span data-stu-id="544cc-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-324">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-325">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-326">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="544cc-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-327">Nome dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-327">Name for the physical element.</span></span>

<span data-ttu-id="544cc-328">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-329">**Nome**</span><span class="sxs-lookup"><span data-stu-id="544cc-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-332">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="544cc-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-333">Etichetta per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="544cc-333">Label for the object.</span></span> <span data-ttu-id="544cc-334">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="544cc-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="544cc-335">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-336">**Number**</span><span class="sxs-lookup"><span data-stu-id="544cc-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-337">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="544cc-339">Numero di slot fisico che può essere usato come indice in una tabella degli slot di sistema, indipendentemente dal fatto che lo slot sia fisicamente vuoto.</span><span class="sxs-lookup"><span data-stu-id="544cc-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="544cc-340">Questo valore deriva dal membro dello **slot ID** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-341">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="544cc-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="544cc-345">Dati aggiuntivi, ovvero più di informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="544cc-346">Un esempio è costituito dai dati del codice a barre associati a un elemento che dispone anche di un tag asset.</span><span class="sxs-lookup"><span data-stu-id="544cc-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="544cc-347">Si noti che se sono disponibili solo i dati del codice a barre ed è univoco o può essere utilizzato come chiave di elemento, questa proprietà è **null** e i dati di codice a barre vengono utilizzati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="544cc-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="544cc-348">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-349">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="544cc-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-352">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="544cc-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-353">Numero di parte che il produttore o il produttore assegna all'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="544cc-354">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="544cc-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-356">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="544cc-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-358">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| slot caratteristiche 2")</span><span class="sxs-lookup"><span data-stu-id="544cc-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-359">Se **true**, questo slot supporta il segnale di risparmio energia (PME) del bus PCI.</span><span class="sxs-lookup"><span data-stu-id="544cc-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="544cc-360">Questo valore deriva dal membro **slot caratteristiche 2** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-361">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="544cc-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-362">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="544cc-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="544cc-364">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="544cc-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="544cc-365">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-366">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="544cc-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-367">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-369">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ slot**](cim-slot.md).**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="544cc-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-370">Stringa in formato libero che descrive il modo in cui questo slot è fisicamente univoco e può mantenere tipi speciali di hardware.</span><span class="sxs-lookup"><span data-stu-id="544cc-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="544cc-371">Questa proprietà ha un significato solo quando la proprietà corrispondente **SpecialPurpose** è **true**.</span><span class="sxs-lookup"><span data-stu-id="544cc-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="544cc-372">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-373">**SegmentGroupNumber**</span><span class="sxs-lookup"><span data-stu-id="544cc-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-374">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="544cc-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-376">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("numero di gruppo di segmenti SMBIOS di \| tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="544cc-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-377">Numero del gruppo di segmenti SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="544cc-378">Questo valore deriva dal membro **numero di gruppo segmento** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-379">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="544cc-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="544cc-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-383">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="544cc-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-384">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="544cc-385">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-386">**Condivisa**</span><span class="sxs-lookup"><span data-stu-id="544cc-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-387">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="544cc-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-389">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| slot Caratteristiche 1")</span><span class="sxs-lookup"><span data-stu-id="544cc-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-390">Se il valore è **true**, due o più slot condividono un percorso sul battiscopa, ad esempio uno slot condiviso PCI/EISA.</span><span class="sxs-lookup"><span data-stu-id="544cc-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="544cc-391">Questo valore deriva dal membro **slot Caratteristiche 1** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="544cc-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-393">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-395">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="544cc-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-396">Numero di unità di stockkeeping per l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="544cc-397">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-398">**SlotDesignation**</span><span class="sxs-lookup"><span data-stu-id="544cc-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-401">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 9 \| slot designation")</span><span class="sxs-lookup"><span data-stu-id="544cc-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-402">Stringa SMBIOS che identifica la designazione dello slot di sistema dello slot sulla scheda madre.</span><span class="sxs-lookup"><span data-stu-id="544cc-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="544cc-403">Esempio: "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="544cc-403">Example: "PCI-1"</span></span>

<span data-ttu-id="544cc-404">Questo valore deriva dal membro della **designazione slot** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="544cc-405">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="544cc-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-406">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="544cc-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-408">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ slot**](cim-slot.md).**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="544cc-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-409">Se **true**, questo slot è fisicamente univoco e può ospitare tipi speciali di hardware, ad esempio uno slot del processore di grafica.</span><span class="sxs-lookup"><span data-stu-id="544cc-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="544cc-410">Se **true**, **PurposeDescription** deve specificare la natura dell'unicità o lo scopo dello slot.</span><span class="sxs-lookup"><span data-stu-id="544cc-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="544cc-411">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="544cc-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-413">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-415">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="544cc-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-416">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="544cc-416">Current status of the object.</span></span> <span data-ttu-id="544cc-417">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="544cc-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="544cc-418">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="544cc-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="544cc-419">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="544cc-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="544cc-420">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="544cc-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="544cc-421">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="544cc-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="544cc-422">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="544cc-423">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="544cc-424">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="544cc-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="544cc-425">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="544cc-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="544cc-426">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="544cc-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="544cc-427">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="544cc-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="544cc-428">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="544cc-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="544cc-429">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="544cc-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="544cc-430">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="544cc-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="544cc-431">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="544cc-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="544cc-432">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="544cc-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="544cc-433">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="544cc-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="544cc-434">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="544cc-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="544cc-435">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="544cc-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="544cc-436">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="544cc-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-437">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="544cc-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-438">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="544cc-439">Se **true**, lo slot supporta il collegamento a caldo delle schede degli adapter.</span><span class="sxs-lookup"><span data-stu-id="544cc-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="544cc-440">Questo valore deriva dal membro **slot caratteristiche 2** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-441">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="544cc-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-443">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-445">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="544cc-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-446">Slot di sistema rappresentato da un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="544cc-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="544cc-447">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="544cc-448">Esempio: "System slot 1"</span><span class="sxs-lookup"><span data-stu-id="544cc-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="544cc-449">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="544cc-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-450">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="544cc-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-452">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot di sistema DMTF \| 004,11 "), [**unità**](../wmisdk/standard-qualifiers.md) (" milliwatt ")</span><span class="sxs-lookup"><span data-stu-id="544cc-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-453">Dissipazione termica massima dello slot in milliwatt.</span><span class="sxs-lookup"><span data-stu-id="544cc-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="544cc-454">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-455">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="544cc-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-456">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="544cc-457">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-458">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot di sistema DMTF \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="544cc-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-459">Matrice di interi enumerati che indica la tensione Vcc supportata da questo slot.</span><span class="sxs-lookup"><span data-stu-id="544cc-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="544cc-460">Questo valore deriva dal membro **slot Caratteristiche 1** della struttura degli **slot di sistema** nelle informazioni SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="544cc-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="544cc-461">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="544cc-462">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="544cc-463">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="544cc-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="544cc-464">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="544cc-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="544cc-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="544cc-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="544cc-466">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="544cc-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="544cc-467">**Versione**</span><span class="sxs-lookup"><span data-stu-id="544cc-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-468">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="544cc-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="544cc-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-470">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="544cc-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="544cc-471">Versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="544cc-471">Version of the physical element.</span></span>

<span data-ttu-id="544cc-472">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="544cc-473">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="544cc-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="544cc-474">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="544cc-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="544cc-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="544cc-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="544cc-476">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot di sistema DMTF \| 004,10 ")</span><span class="sxs-lookup"><span data-stu-id="544cc-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="544cc-477">Matrice di interi enumerati che indica la tensione VPP supportata da questo slot.</span><span class="sxs-lookup"><span data-stu-id="544cc-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="544cc-478">Questa proprietà viene ereditata [**dallo \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="544cc-479">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="544cc-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="544cc-480">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="544cc-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="544cc-481">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="544cc-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="544cc-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="544cc-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="544cc-483">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="544cc-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="544cc-484">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="544cc-484">**12V** (4)</span></span>


<span data-ttu-id="544cc-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="544cc-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="544cc-486">Commenti</span><span class="sxs-lookup"><span data-stu-id="544cc-486">Remarks</span></span>

<span data-ttu-id="544cc-487">La classe **Win32 \_ SystemSlot** è derivata dallo [**\_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="544cc-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="544cc-488">Requisiti</span><span class="sxs-lookup"><span data-stu-id="544cc-488">Requirements</span></span>



| <span data-ttu-id="544cc-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="544cc-489">Requirement</span></span> | <span data-ttu-id="544cc-490">Valore</span><span class="sxs-lookup"><span data-stu-id="544cc-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="544cc-491">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="544cc-491">Minimum supported client</span></span><br/> | <span data-ttu-id="544cc-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="544cc-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="544cc-493">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="544cc-493">Minimum supported server</span></span><br/> | <span data-ttu-id="544cc-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="544cc-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="544cc-495">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="544cc-495">Namespace</span></span><br/>                | <span data-ttu-id="544cc-496">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="544cc-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="544cc-497">MOF</span><span class="sxs-lookup"><span data-stu-id="544cc-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="544cc-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="544cc-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="544cc-499">DLL</span><span class="sxs-lookup"><span data-stu-id="544cc-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="544cc-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="544cc-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="544cc-501">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="544cc-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544cc-502">**\_Slot CIM**</span><span class="sxs-lookup"><span data-stu-id="544cc-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="544cc-503">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="544cc-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
