---
description: La \_ classe CIM PhysicalConnector rappresenta qualsiasi elemento fisico usato per connettersi ad altri elementi. Qualsiasi oggetto in grado di connettersi e trasmettere segnali o potere tra due o più elementi fisici è un discendente (o membro) di questa classe.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: Classe CIM_PhysicalConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304971"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="a6347-104">CIM \_ PhysicalConnector (classe)</span><span class="sxs-lookup"><span data-stu-id="a6347-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="a6347-105">La classe **CIM \_ PhysicalConnector** rappresenta qualsiasi elemento fisico usato per connettersi ad altri elementi.</span><span class="sxs-lookup"><span data-stu-id="a6347-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="a6347-106">Qualsiasi oggetto in grado di connettersi e trasmettere segnali o potere tra due o più elementi fisici è un discendente (o membro) di questa classe.</span><span class="sxs-lookup"><span data-stu-id="a6347-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="a6347-107">Ad esempio, slot e connettori D-shell sono tipi di connettori fisici.</span><span class="sxs-lookup"><span data-stu-id="a6347-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6347-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a6347-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a6347-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a6347-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a6347-110">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a6347-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a6347-111">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a6347-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6347-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6347-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="a6347-113">Members</span><span class="sxs-lookup"><span data-stu-id="a6347-113">Members</span></span>

<span data-ttu-id="a6347-114">La classe **CIM \_ PhysicalConnector** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a6347-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="a6347-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6347-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6347-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a6347-116">Properties</span></span>

<span data-ttu-id="a6347-117">La classe **CIM \_ PhysicalConnector** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a6347-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6347-118">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a6347-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-121">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a6347-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a6347-122">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6347-122">A short textual description of the object.</span></span>

<span data-ttu-id="a6347-123">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-124">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="a6347-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6347-127">Stringa in formato libero che descrive la configurazione del PIN e l'uso del segnale di un connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="a6347-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="a6347-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-129">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6347-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6347-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6347-131">Tipo di connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-131">Type of physical connector.</span></span> <span data-ttu-id="a6347-132">Viene specificata una matrice per consentire la descrizione delle combinazioni di informazioni del connettore.</span><span class="sxs-lookup"><span data-stu-id="a6347-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="a6347-133">Una voce della matrice, ad esempio, può specificare RS-232, un altro DB-25 e una terza voce può definire il connettore come "maschio".</span><span class="sxs-lookup"><span data-stu-id="a6347-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6347-134">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a6347-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a6347-135">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a6347-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="a6347-136">**Maschio** (2)</span><span class="sxs-lookup"><span data-stu-id="a6347-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="a6347-137">**Female** (3)</span><span class="sxs-lookup"><span data-stu-id="a6347-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="a6347-138">**Schermato** (4)</span><span class="sxs-lookup"><span data-stu-id="a6347-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="a6347-139">Non **schermato** (5)</span><span class="sxs-lookup"><span data-stu-id="a6347-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="a6347-140">**SCSI (A) High-Density (50 pin)** (6)</span><span class="sxs-lookup"><span data-stu-id="a6347-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="a6347-141">**SCSI (A) Low-Density (50 pin)** (7)</span><span class="sxs-lookup"><span data-stu-id="a6347-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="a6347-142">**High-Density SCSI (P) (68 pin)** (8)</span><span class="sxs-lookup"><span data-stu-id="a6347-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="a6347-143">**SCSI SCA-I (80 pin)** (9)</span><span class="sxs-lookup"><span data-stu-id="a6347-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="a6347-144">**SCSI SCA-II (80 pin)** (10)</span><span class="sxs-lookup"><span data-stu-id="a6347-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="a6347-145">**Fibre Channel SCSI (DB-9, rame)** (11)</span><span class="sxs-lookup"><span data-stu-id="a6347-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="a6347-146">**Fibre Channel SCSI (fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="a6347-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="a6347-147">**SCSI Fibre Channel SCA-II (40 pin)** (13)</span><span class="sxs-lookup"><span data-stu-id="a6347-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="a6347-148">**SCSI Fibre Channel SCA-II (20 pin)** (14)</span><span class="sxs-lookup"><span data-stu-id="a6347-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="a6347-149">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="a6347-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="a6347-150">**ATA 3-1/2 pollice (40 pin)** (16)</span><span class="sxs-lookup"><span data-stu-id="a6347-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="a6347-151">**ATA 2-1/2 inch (44 pin)** (17)</span><span class="sxs-lookup"><span data-stu-id="a6347-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="a6347-152">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="a6347-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="a6347-153">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="a6347-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="a6347-154">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="a6347-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="a6347-155">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="a6347-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="a6347-156">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="a6347-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="a6347-157">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="a6347-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="a6347-158">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="a6347-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="a6347-159">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="a6347-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="a6347-160">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="a6347-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="a6347-161">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="a6347-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="a6347-162">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="a6347-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="a6347-163">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="a6347-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="a6347-164">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="a6347-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="a6347-165">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="a6347-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="a6347-166">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="a6347-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="a6347-167">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="a6347-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="a6347-168">**Categoria UTP 3** (34)</span><span class="sxs-lookup"><span data-stu-id="a6347-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="a6347-169">**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="a6347-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="a6347-170">**Categoria UTP 5** (36)</span><span class="sxs-lookup"><span data-stu-id="a6347-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="a6347-171">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="a6347-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="a6347-172">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="a6347-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="a6347-173">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="a6347-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="a6347-174">**Fiber MIC** (40)</span><span class="sxs-lookup"><span data-stu-id="a6347-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="a6347-175">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="a6347-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="a6347-176">**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="a6347-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="a6347-177">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="a6347-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="a6347-178">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="a6347-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="a6347-179">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="a6347-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="a6347-180">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="a6347-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="a6347-181">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="a6347-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="a6347-182">**Tipi PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="a6347-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="a6347-183">**Tipo PCMCIA II** (49)</span><span class="sxs-lookup"><span data-stu-id="a6347-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="a6347-184">**Tipo PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="a6347-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="a6347-185">**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="a6347-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="a6347-186">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="a6347-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="a6347-187">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="a6347-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="a6347-188">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="a6347-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="a6347-189">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="a6347-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="a6347-190">**HSSDC (6 pin)** (56)</span><span class="sxs-lookup"><span data-stu-id="a6347-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="a6347-191">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="a6347-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="a6347-192">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="a6347-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="a6347-193">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="a6347-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="a6347-194">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="a6347-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="a6347-195">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="a6347-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="a6347-196">**Infrarossi** (62)</span><span class="sxs-lookup"><span data-stu-id="a6347-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="a6347-197">**HP-** b (63)</span><span class="sxs-lookup"><span data-stu-id="a6347-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="a6347-198">**Access. bus** (64)</span><span class="sxs-lookup"><span data-stu-id="a6347-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="a6347-199">**Nubus** (65)</span><span class="sxs-lookup"><span data-stu-id="a6347-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="a6347-200">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="a6347-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="a6347-201">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="a6347-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="a6347-202">**Tipo Mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="a6347-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="a6347-203">**Tipo Mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="a6347-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="a6347-204">**Tipo Mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="a6347-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="a6347-205">**Mouse bus** (71)</span><span class="sxs-lookup"><span data-stu-id="a6347-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="a6347-206">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="a6347-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="a6347-207">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="a6347-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="a6347-208">**Bus VME** (74)</span><span class="sxs-lookup"><span data-stu-id="a6347-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="a6347-209">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="a6347-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="a6347-210">**Proprietario** (76)</span><span class="sxs-lookup"><span data-stu-id="a6347-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="a6347-211">**Slot scheda processore proprietario** (77)</span><span class="sxs-lookup"><span data-stu-id="a6347-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="a6347-212">**Slot scheda di memoria proprietaria** (78)</span><span class="sxs-lookup"><span data-stu-id="a6347-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="a6347-213">**Slot di riser I/O proprietario** (79)</span><span class="sxs-lookup"><span data-stu-id="a6347-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="a6347-214">**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="a6347-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="a6347-215">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="a6347-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="a6347-216">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="a6347-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="a6347-217">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="a6347-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="a6347-218">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="a6347-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="a6347-219">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="a6347-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="a6347-220">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="a6347-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="a6347-221">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="a6347-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="a6347-222">**SCSI ssa** (88)</span><span class="sxs-lookup"><span data-stu-id="a6347-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="a6347-223">**Circolare** (89)</span><span class="sxs-lookup"><span data-stu-id="a6347-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="a6347-224">**Connettore IDE a bordo** (90)</span><span class="sxs-lookup"><span data-stu-id="a6347-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="a6347-225">**Connettore floppy a bordo** (91)</span><span class="sxs-lookup"><span data-stu-id="a6347-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="a6347-226">**2 pin doppio inline** (92)</span><span class="sxs-lookup"><span data-stu-id="a6347-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="a6347-227">**25 pin doppio inline** (93)</span><span class="sxs-lookup"><span data-stu-id="a6347-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="a6347-228">**Pin 50 dual inline** (94)</span><span class="sxs-lookup"><span data-stu-id="a6347-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="a6347-229">**Pin 68 dual inline** (95)</span><span class="sxs-lookup"><span data-stu-id="a6347-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="a6347-230">**Connettore audio a bordo** (96)</span><span class="sxs-lookup"><span data-stu-id="a6347-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="a6347-231">**Mini-jack** (97)</span><span class="sxs-lookup"><span data-stu-id="a6347-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="a6347-232">**PCI-X** (98)</span><span class="sxs-lookup"><span data-stu-id="a6347-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="a6347-233">**SBus IEEE 1396-1993 32 bit** (99)</span><span class="sxs-lookup"><span data-stu-id="a6347-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="a6347-234">**SBus IEEE 1396-1993 64 bit** (100)</span><span class="sxs-lookup"><span data-stu-id="a6347-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="a6347-235">**MCA** (101)</span><span class="sxs-lookup"><span data-stu-id="a6347-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="a6347-236">**Gio** (102)</span><span class="sxs-lookup"><span data-stu-id="a6347-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="a6347-237">**XIO** (103)</span><span class="sxs-lookup"><span data-stu-id="a6347-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="a6347-238">**Hio** (104)</span><span class="sxs-lookup"><span data-stu-id="a6347-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="a6347-239">**NGIO** (105)</span><span class="sxs-lookup"><span data-stu-id="a6347-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="a6347-240">**PMC** (106)</span><span class="sxs-lookup"><span data-stu-id="a6347-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="a6347-241">**MTRJ** (107)</span><span class="sxs-lookup"><span data-stu-id="a6347-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="a6347-242">**VF-45** (108)</span><span class="sxs-lookup"><span data-stu-id="a6347-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="a6347-243">**I/O futuro** (109)</span><span class="sxs-lookup"><span data-stu-id="a6347-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="a6347-244">**SC** (110)</span><span class="sxs-lookup"><span data-stu-id="a6347-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="a6347-245">**SG** (111)</span><span class="sxs-lookup"><span data-stu-id="a6347-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="a6347-246">**Elettrico** (112)</span><span class="sxs-lookup"><span data-stu-id="a6347-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="a6347-247">**Ottico** (113)</span><span class="sxs-lookup"><span data-stu-id="a6347-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="a6347-248">**Barra multifunzione** (114)</span><span class="sxs-lookup"><span data-stu-id="a6347-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="a6347-249">**GLM** (115)</span><span class="sxs-lookup"><span data-stu-id="a6347-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="a6347-250">**1x9** (116)</span><span class="sxs-lookup"><span data-stu-id="a6347-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="a6347-251">**Mini SG** (117)</span><span class="sxs-lookup"><span data-stu-id="a6347-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="a6347-252">**LC** (118)</span><span class="sxs-lookup"><span data-stu-id="a6347-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="a6347-253">**Hssc** (119)</span><span class="sxs-lookup"><span data-stu-id="a6347-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="a6347-254">**Schermate VHDCI (68 pin)** (120)</span><span class="sxs-lookup"><span data-stu-id="a6347-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="a6347-255">**InfiniBand** (121)</span><span class="sxs-lookup"><span data-stu-id="a6347-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6347-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6347-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-259">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a6347-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-260">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a6347-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a6347-261">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a6347-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a6347-262">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-263">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a6347-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-266">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="a6347-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a6347-267">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6347-267">A textual description of the object.</span></span>

<span data-ttu-id="a6347-268">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6347-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-270">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6347-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-272">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="a6347-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a6347-273">Indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="a6347-273">Indicates when the object was installed.</span></span> <span data-ttu-id="a6347-274">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="a6347-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a6347-275">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-276">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="a6347-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-279">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a6347-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-280">Nome dell'organizzazione responsabile della creazione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="a6347-281">Per ulteriori informazioni, vedere la proprietà **Vendor** del [**\_ prodotto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="a6347-282">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-283">**Modello**</span><span class="sxs-lookup"><span data-stu-id="a6347-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-286">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a6347-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-287">Nome in base al quale l'elemento fisico è generalmente noto.</span><span class="sxs-lookup"><span data-stu-id="a6347-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="a6347-288">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-289">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a6347-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-292">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a6347-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6347-293">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="a6347-293">Label by which the object is known.</span></span> <span data-ttu-id="a6347-294">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="a6347-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a6347-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="a6347-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6347-299">Dati aggiuntivi, oltre alle informazioni sui tag asset, che possono essere usati per identificare un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="a6347-300">Un esempio è costituito dai dati del codice a barre associati a un elemento, che include anche un tag asset.</span><span class="sxs-lookup"><span data-stu-id="a6347-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="a6347-301">Si noti che se sono disponibili solo dati del codice a barre ed è univoco e può essere usato come chiave dell'elemento, questa proprietà sarà null e i dati del codice a barre verrebbero usati come chiave della classe nella proprietà **tag** .</span><span class="sxs-lookup"><span data-stu-id="a6347-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="a6347-302">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-303">**NumeroArticolo**</span><span class="sxs-lookup"><span data-stu-id="a6347-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-306">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a6347-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-307">Numero di parte assegnato dall'organizzazione responsabile della produzione o della produzione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="a6347-308">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-309">**PoweredOn**</span><span class="sxs-lookup"><span data-stu-id="a6347-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-310">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a6347-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6347-312">Se **true**, l'elemento fisico è acceso.</span><span class="sxs-lookup"><span data-stu-id="a6347-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="a6347-313">In caso contrario, è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="a6347-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="a6347-314">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-315">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a6347-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-316">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-318">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a6347-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-319">Numero allocato dal produttore utilizzato per identificare l'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="a6347-320">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-321">**SKU**</span><span class="sxs-lookup"><span data-stu-id="a6347-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-322">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-324">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a6347-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-325">Numero di unità di conservazione per questo elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="a6347-326">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-327">**Status**</span><span class="sxs-lookup"><span data-stu-id="a6347-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-330">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a6347-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a6347-331">Stringa che indica lo stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a6347-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="a6347-332">È possibile definire lo stato operativo e non operativo.</span><span class="sxs-lookup"><span data-stu-id="a6347-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a6347-333">Lo stato operativo può includere "OK", "danneggiato" e "errore predazione".</span><span class="sxs-lookup"><span data-stu-id="a6347-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a6347-334">"Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.</span><span class="sxs-lookup"><span data-stu-id="a6347-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a6347-335">Lo stato non operativo può includere "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="a6347-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a6347-336">Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="a6347-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a6347-337">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="a6347-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a6347-338">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a6347-339">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6347-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a6347-340">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a6347-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a6347-341">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="a6347-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a6347-342">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="a6347-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6347-343">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="a6347-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a6347-344">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="a6347-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a6347-345">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="a6347-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a6347-346">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="a6347-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a6347-347">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="a6347-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a6347-348">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="a6347-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a6347-349">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="a6347-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a6347-350">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="a6347-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a6347-351">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="a6347-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6347-352">**Tag**</span><span class="sxs-lookup"><span data-stu-id="a6347-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-355">Qualificatori: [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a6347-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-356">Identifica in modo univoco l'elemento fisico e funge da chiave dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a6347-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="a6347-357">Questa proprietà può contenere informazioni, ad esempio i dati del tag asset o del numero di serie.</span><span class="sxs-lookup"><span data-stu-id="a6347-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="a6347-358">La chiave per [**CIM \_ PhysicalElement**](cim-physicalelement.md) è posizionata in modo molto elevato nella gerarchia degli oggetti per identificare in modo indipendente l'hardware o l'entità, indipendentemente dalla posizione fisica nei cabinet, nelle schede e così via.</span><span class="sxs-lookup"><span data-stu-id="a6347-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="a6347-359">Ad esempio, un componente rimovibile che può essere scambiato a caldo può essere tratto dal pacchetto contenitore (ambito) ed essere temporaneamente inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="a6347-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="a6347-360">L'oggetto continua a esistere e può anche essere inserito in un altro contenitore di ambito.</span><span class="sxs-lookup"><span data-stu-id="a6347-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="a6347-361">La chiave per un elemento fisico è una stringa arbitraria definita indipendentemente dal posizionamento o dalla gerarchia orientata alla posizione.</span><span class="sxs-lookup"><span data-stu-id="a6347-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="a6347-362">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6347-363">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a6347-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6347-364">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a6347-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6347-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a6347-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6347-366">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a6347-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6347-367">Indica la versione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a6347-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="a6347-368">Questa proprietà viene ereditata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6347-369">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6347-369">Remarks</span></span>

<span data-ttu-id="a6347-370">La classe **CIM \_ PhysicalConnector** è derivata da [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="a6347-371">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a6347-371">WMI does not implement this class.</span></span> <span data-ttu-id="a6347-372">Per le classi WMI derivate da **CIM \_ PhysicalConnector**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a6347-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a6347-373">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a6347-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a6347-374">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a6347-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6347-375">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6347-375">Requirements</span></span>



| <span data-ttu-id="a6347-376">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6347-376">Requirement</span></span> | <span data-ttu-id="a6347-377">Valore</span><span class="sxs-lookup"><span data-stu-id="a6347-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6347-378">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6347-378">Minimum supported client</span></span><br/> | <span data-ttu-id="a6347-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6347-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6347-380">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6347-380">Minimum supported server</span></span><br/> | <span data-ttu-id="a6347-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6347-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6347-382">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6347-382">Namespace</span></span><br/>                | <span data-ttu-id="a6347-383">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a6347-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6347-384">MOF</span><span class="sxs-lookup"><span data-stu-id="a6347-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6347-385"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6347-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6347-386">DLL</span><span class="sxs-lookup"><span data-stu-id="a6347-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6347-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6347-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6347-388">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6347-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6347-389">**\_PhysicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="a6347-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

